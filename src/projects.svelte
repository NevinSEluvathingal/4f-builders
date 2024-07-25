<script>
	let images = [
		{
			url: 'p.png',
			details: {
				'Project Name': ' Double Storage House 2450 Sq. Feet',
				Client: ' Mr.Kunjumon N.R',
				'Project Consultant': '4f Builders',
				'Project Value': ' 59 Lakhs',
				'Project Duration': '13 months',
				Location: ' Keerukuzhi, Thumpamon, Pathanamthitta'
			}
		},
		{
			url: 'p (2).png',
			details: {
				'Project Name': 'Interior work',
				Client: 'Mr.Anil Kumar',
				'Project Consultant': '4f Builders',
				'Project Value': '20 Lakhs',
				'Project Duration': '6 months',
				Location: ' Chengannur Alappuzha'
			}
		},
		{
			url: 'p (3).png',
			details: {
				'Project Name': 'Single Storage House 1500 Sq. Feet',
				Client: ' Mr.Satheesan',
				'Project Consultant': '4f Builders',
				'Project Value': '30 Lakhs',
				'Project Duration': '6 months',
				Location: ' Pandalam Pathanamthitta'
			}
		},
		{
			url: 'p (4).png',
			details: {
				'Project Name': ' (PEB) Warehouse 1152 Sq.M',
				Client: ' Al-Khalawi Engineering',
				'Project Consultant': 'Mashoor',
				'Project Value': '150,000 OMR',
				'Project Duration': '6 months',
				Location: ' Sohar Oman'
			}
		},
		{
			url: 'p (5).png',
			details: {
				'Project Name': 'House 2650 Sq. Feet',
				Client: ' Mr. Aneesh',
				'Project Consultant': 'Sree Ram',
				'Project Value': '14 lakhs',
				'Project Duration': '9 months',
				Location: ' Chengannur'
			}
		},
		{
			url: 'p (6).png',
			details: {
				'Project Name': 'G+2 Residential Bldg.',
				Client: '  Mr. Khalid AmurAl Badi',
				'Project Consultant': '4f Builders',
				'Project Value': '126000 OMR',
				'Project Duration': '9 months',
				Location: ' Sohar Oman'
			}
		},
		{
			url: 'p (7).png',
			details: {
				'Project Name': 'G+3 Residential Bldg.',
				Client: ' Mr. Fatima Bin Shafi',
				'Project Consultant': '4f Builders',
				'Project Value': '168000 OMR',
				'Project Duration': '11 months',
				Location: ' Sohar Oman'
			}
		},
		{
			url: 'p (8).png',
			details: {
				'Project Name': 'Villa 2450 Sq. M',
				Client: 'Shabina Koroth',
				'Project Consultant': '4f Builders',
				'Project Value': '50 Lakhs',
				'Project Duration': '16 months',
				Location: ' Kannur, Kerala'
			}
		},
		{
			url: 'p (9).png',
			details: {
				'Project Name': 'Flood relief houses x 6 Nos',
				Client: 'Sri Sathya Sai Trust, Kerala',
				'Project Consultant': '4f Builders',
				'Project Value': '55 Lakhs',
				'Project Duration': '10 months',
				Location: ' Noornad, Alappuzha, Kerala'
			}
		},
		{
			url: 'p (10).png',
			details: {
				'Project Name': 'Anganwadi x 6 Nos',
				Client: 'Sri Sathya Sai Trust, Kerala',
				'Project Consultant': '4f Builders',
				'Project Value': '55 Lakhs',
				'Project Duration': '13 months',
				Location: ' Noornad, Alappuzha, Kerala'
			}
		},
		{
			url: 'p (11).png',
			details: {
				'Project Name': 'Villa 1395 Sq. Feet',
				Client: 'Ashish Nooranadu',
				'Project Consultant': '4f Builders',
				'Project Value': '40 Lakhs',
				'Project Duration': '10 months',
				Location: ' Noornad, Alappuzha, Kerala'
			}
		},
		
	];

	let currentIndex = 0;

	function nextImage() {
		currentIndex = (currentIndex + 1) % images.length;
	}

	function prevImage() {
		currentIndex = (currentIndex - 1 + images.length) % images.length;
	}
</script>

<div class="slideshow">
	<div class="image-container">
		<img src={images[currentIndex].url} alt="" />
	</div>

	<div class="text-container">
		<div class="image-text">
			<table>
				<thead>
					<tr>
						<th colspan="2">Project Details</th>
					</tr>
				</thead>
				<tbody>
					{#each Object.entries(images[currentIndex].details) as [key, value]}
						<tr>
							<td>{key}</td>
							<td>{value}</td>
						</tr>
					{/each}
				</tbody>
			</table>
		</div>
	</div>

	<div class="controls">
		<button on:click={prevImage}>Previous</button>
		<button on:click={nextImage}>Next</button>
	</div>
</div>

<style>
	.slideshow {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		height: 100vh;
		overflow: hidden;
		position: relative;
		background-color: #0F4C75;
	}

	.image-container {
		align-items: center;
	align-content: center;
		margin-top: 20px;
		width: 1000px;
		height: 445px;
		margin-bottom: 30px;
		border-radius: 10px; 
		overflow: hidden; 
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); 
	}

	img {
		width: 1000px;
		height: 450px;
		border-radius: 10px; 
	}

	.text-container {
		width: 1000px;
    margin-bottom: 10px;
	}

	.image-text {
		background-color: rgba(0, 0, 0, 0.7);
		color: white;
		padding: 10px; 
		border-radius: 5px;
		font-family: DM SANS;}

	.image-text table {
		width: 100%; 
		border-collapse: collapse;
	}

	.image-text th,
	.image-text td {
		border: 1px solid white; 
		padding: 10px;
		font-size: 16px; 
		width: 120px;
	}

	.controls {
		position: absolute;
		bottom: 10px;
		left: 50%;
		transform: translateX(-50%);
	}

	button {
		margin: 0 10px; 
		padding: 10px 20px; 
		background-color: #1B262C; 
		color: white;
		border: none;
		border-radius: 5px;
		cursor: pointer;
		font-size: 18px; 
		transition: background-color 0.3s; 
	}

	button:hover {
		background-color: #4a5568; 
	}
</style>
