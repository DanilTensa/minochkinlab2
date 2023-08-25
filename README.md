<div id="parent">
	<div id="calendar">
		<div class="info">Jan 2020</div>
		<table>
			<thead>
				<tr>
					<th>Mon</th>
					<th>Tue</th>
					<th>Wed</th>
					<th>Thu</th>
					<th>Fri</th>
					<th>Sat</th>
					<th>Sun</th>
				</tr>
			</thead>
			<tbody class="body"></tbody>
		</table>
		<div class="nav">
			<a href="#" class="prev">←</a>
			<a href="#" class="next">→</a>
		</div>
	</div>
</div>
#parent {
	text-align: center;
}
#calendar {
	display: inline-block;
}
#calendar td, #calendar th {
	padding: 10px;
	border: 1px solid black;
	text-align: center;
}

#calendar .nav, #calendar .info {
	text-align: center;
}
#calendar a {
	color: blue;
	font-size: 25px;
	text-decoration: none;
}
#calendar a:hover {
	color: red;
}

#calendar .active {
	color: red;
}


let prev = calendar.querySelector('.prev');
let next = calendar.querySelector('.next');


next.addEventListener('click', function() {
	draw(body, getNextYear(year, month), getNextMonth(month));
});


prev.addEventListener('click', function() {
	draw(body, getPrevYear(year, month), getPrevMonth(month));
});
