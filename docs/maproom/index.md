---
layout: default
title: "Happy Jekylling!"
---

<html>
<head>

	<title>Million Dollar Hoods Maproom v2</title>

	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0">

	<!-- leaflet  -->
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css" integrity="sha512-Rksm5RenBEKSKFjgI3a41vrjkw4EVPlJ3+OiI65vTjIdo9brlAacEuKOiQ5OFh7cOI1bkDwLqdLw3Zg0cRJAAQ==" crossorigin=""/>
	<script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet.js" integrity="sha512-/Nsx9X4HebavoBvEBuyp3I7od5tA0UzAxs+j83KgC8PU0kgB4XiK4Lfe4y4cgBtaRJQEIFCW+oC506aPT2L1zw==" crossorigin=""></script>

	<!-- jQuery -->
	<script src="https://code.jquery.com/jquery-1.10.2.js"></script>
	<script src="js/libraries/list.min.js"></script>

	  <!-- data table -->
	<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.19/css/jquery.dataTables.css">
	<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.19/js/jquery.dataTables.js"></script>
	<!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script> -->
	<!-- bootstrap -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>

	<script src="js/rangeSlider/js/ion-rangeSlider/ion.rangeSlider.min.js" type="text/javascript"></script>
	<link rel="stylesheet" href="js/rangeSlider/css/ion.rangeSlider.css">
	<link rel="stylesheet" href="js/rangeSlider/css/ion.rangeSlider.skinFlat.css">

	<link rel="stylesheet" href="styles/style.css">

</head>
<body>

<div class="container-fluid h-100">
	<div class="row h-100">
		<!-- left side: map -->
		<div class="col-sm fill no-padding">
			<div id="map"></div>
			<div id="slider-container">
				<input type="text" id="slider" name="millionDollarSlider" value="" />
			</div><!-- <div class='nav-overlay'></div> -->
		</div>

		<!-- right side: data -->
		<div class="col-sm " id="data-panel">
			<br>
			<div class='nav-overlay'></div>
			<p class="lead" id="data-subtitle"></p>

			<div class="">
				<ul class="nav nav-tabs" id="myTab" role="tablist">
					<li class="nav-item">
						<a class="nav-link active" id="prison-tab" data-toggle="tab" href="#prison" role="tab" aria-controls="prison" aria-selected="true">Jail Data</a>
					</li>
					<!-- charges are turned off for now -->
					<!--
					<li class="nav-item">
						<a class="nav-link" id="charges-tab" data-toggle="tab" href="#charges" role="tab" aria-controls="charges" aria-selected="false">Charges</a>
					</li>
					 -->
					<li class="nav-item">
						<a class="nav-link" id="rankings-tab" data-toggle="tab" href="#rankings" role="tab" aria-controls="rankings" aria-selected="false">Rankings</a>
					</li>
				</ul>
				<div class="tab-content" id="myTabContent">
					<br>
					<div class="tab-pane fade show active" id="prison" role="tabpanel" aria-labelledby="prison-tab">
						<div style="clear:both" id="stats-content-prison1">
						</div>
						<div style="clear:both" id="stats-content-prison2"></div>

						<h1 class="display-4" id="data-title"></h1>
						<div class="container">
							<div class="row" id="data-text1">
								<div class="alert alert-dark">
									On the map to the left, hover your mouse on neighborhoods to learn how much LASD and LAPD spent to incarcerate residents of that community between 2012 and 2017.  With each click you will also access supplemental data, such as the leading causes of arrest within each neighborhood and the racial and gender demographics of arrested persons.
								</div>
							</div>
							<div class="row" id="data-text2"></div>
						</div>

					</div>
					<!-- charges turned off for now -->
					<!--
					<div class="tab-pane fade" id="charges" role="tabpanel" aria-labelledby="charges-tab">
					</div>
					 -->
					<div class="tab-pane fade" id="rankings" role="tabpanel" aria-labelledby="rankings-tab">

					</div>
				</div>

			</div>
		</div>
	</div>
</div>

<script type="text/javascript" src="js/mdbla.config.js"></script>
<script type="text/javascript" src="js/mdbla.rankings.js"></script>

</body>
</html>
