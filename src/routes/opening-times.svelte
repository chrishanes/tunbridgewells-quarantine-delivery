<script>
	export let data = [
		{
			header: "Camden Road",
			shops: [
				{
					name: "Bicycle Bakery",
					items: ["Tuesday to Saturday 8am - 2pm"]
				},
				{
					name: "Camden Butchers",
					items: ["Tuesday to Thursday 10am - 3pm", "Friday & Saturday 8am - 1pm"]
				},
				{
					name: "Camden News",
					items: ["Monday to Saturday 7am - 7pm", "Sunday 8am - 4pm"]
				},
				{
					name: "Charcoal Grill",
					items: ["Monday to Sunday 12pm - 11pm"]
				},
				{
					name: "Helios Homeopathy",
					items: ["Monday to Friday 9am - 5pm", "Saturday 10am - 2pm"]
				},
				{
					name: "Locality Fruit & Veg",
					items: ["Monday to Saturday 8am - 6pm"]
				},
				{
					name: "The International Shop",
					items: ["Monday to Saturday 10am - 7pm", "Sunday 11am - 5pm"]
				},
				{
					name: "Topps Pizza",
					items: ["Monday to Sunday 11:30am - Midnight"]
				},
				{
					name: "Tunbridge Wells Fish & Chips",
					items: ["Sunday to Thursday 12pm - 9pm", "Friday & Saturday 12pm - 10pm"]
				},
				{
					name: "Velocipede Cycles",
					items: ["Monday to Saturday 10am - 4pm"]
				},
				{
					name: "Wildside Cycles",
					items: ["Monday to Saturday 9am - 6pm", "Sunday 10am - 4pm"]
				}
			]
		},
		{
			header: "Monson Road",
			shops: [
				{
					name: "Cook",
					items: ["Monday to Saturday 9:30am - 4:30pm", "Sunday 10:30am - 3:30pm"]
				},
				{
					name: "Monson News",
					items: ["Monday to Saturday 7:30am - 6pm", "Sunday 10am - 2pm"]
				},
				{
					name: "Wolfit Pet Shop",
					items: ["Monday to Saturday 9am - 5pm"]
				}
			]
		},
		{
			header: "Grosvenor Road",
			shops: [
				{
					name: "Charcoal Grill",
					items: ["Monday to Sunday 12pm - 12am"]
				},
				{
					name: "Poundland",
					items: ["Monday to Saturday 9am - 6pm", "Sunday 10am - 4pm"]
				},
				{
					name: "Salt & Vinegar Fish & Chips",
					items: ["Monday to Saturday 11:30am - 10:30pm", "Sunday 1pm - 9pm"]
				},
				{
					name: "Tesco Metro",
					items: ["Monday to Thursday 7am - 8pm", "Friday & Saturday 7am -9pm", "Sunday 10am - 4pm"]
				},
				{
					name: "Zorba Meze Grill",
					items: ["Monday to Sunday 12pm - 10pm"]
				}
			]
		},
		{
			header: "Calverley Road & Royal Victoria Place",
			shops: [
				{
					name: "Boots",
					items: ["Monday to Saturday 9am - 6pm", "Sunday 10:30am - 4:30pm"]
				},
				{
					name: "Grape Tree Health Food",
					items: ["Monday to Saturday 9am - 4pm"]
				},
				{
					name: "Holland & Barratt",
					items: ["Monday to Sunday 9am - 4pm"]
				},
				{
					name: "Marks & Spencer",
					items: ["Monday to Saturday 9am - 6pm", "Sunday 10:30am - 4:30pm"]
				},
				{
					name: "Superdrug",
					items: ["Monday to Saturday 9am - 4pm", "Sunday 10:30am - 4:30pm"]
				},
				{
					name: "Wilkinsons",
					items: ["Monday to Saturday 9am - 5pm", "Sunday 10:30am - 4:30pm"]
				}
			]
		},
		{
			header: "Mount Pleasant Road",
			shops: [
				{
					name: "A E Hobbs Pharmacy",
					items: ["Monday to Saturday 9am - 5:30pm"]
				},
				{
					name: "Royal Express",
					items: ["Monday to Sunday 4pm - Midnight"]
				},
				{
					name: "Sainsburys Local",
					items: ["Monday to Saturday 7am - 9pm", "Sunday 12pm - 6pm"]
				}
			]
		},
		{
			header: "High Street",
			shops: [
				{
					name: "Arte Bianca",
					items: ["Tuesday to Saturday 9am - 4pm"]
				},
				{
					name: "Best Health Food Shop",
					items: ["Monday to Saturday 9am - 5:30pm", "Sunday 11am - 4pm"]
				},
				{
					name: "McColls",
					items: ["Monday to Sunday 8am - 8pm"]
				}
			]
		},
		{
			header: "The Pantiles",
			shops: [
				{
					name: "Imperial Pharmacy",
					items: ["Monday to Saturday 9am - 1pm & 2pm - 5pm"]
				},
				{
					name: "Pantiles News",
					items: ["Monday to Saturday 8:30am - 4pm", "Sunday 7am - 4pm"]
				},
				{
					name: "The Pantiles Tap",
					items: ["Tuesday to Sunday 3pm - 7pm"]
				},
				{
					name: "Zero Waste Company",
					items: ["Tuesday to Saturday 11am - 3pm", "Sunday 10am - 1pm"]
				}
			]
		},
		{
			header: "Other Locations",
			shops: [
				{
					name: "Sainsburys, Linden Park Road",
					items: ["Monday to Saturday 8am - 10pm", "Sunday 10am - 4pm"]
				},
				{
					name: "Zavens, Mount Ephraim",
					items: ["Monday to Saturday 10am - 5pm"]
				}
			]
		}
	];
</script>

<style>
	.grid-col-12 {
		grid-column: span 12;
	}

	.card {
        border: 1px solid var(--gold);
        border-radius: 20px;
        color: var(--blue);
        grid-column: span 12;
        padding: 15px 20px;
    }

    @media (min-width: 480px) {
        .card {
            grid-column: span 6;
        }
    }

    @media (min-width: 1024px) {
        .card {
            grid-column: span 4;
        }
    }

    @media (min-width: 1280px) {
        .card {
            grid-column: span 3;
        }
    }

    .card__title {
        font-family: var(--title-font);
        margin-bottom: 5px;
        text-align: center;
        text-transform: uppercase;
    }

    .card-item {
        display: flex;
        margin-top: 10px;
    }

    .card-item__icon {
        fill: var(--gold);
        height: 20px;
        min-width: 20px;
        width: 20px;
    }

    .card-item__icon--category {
        height: 20px;
    }

    .card-item__text {
        font-size: 1.4rem;
        margin-left: 10px;
    }
</style>

<div class="grid-col-12">
	<h1>Opening times</h1>
	<p>The following businesses are open in the town centre and serving local residents. Please shop sensibly and observe correct social distancing.</p>
</div>

{#each data as section}
	<h2 class="grid-col-12">{section.header}</h2>
	{#each section.shops as shop}
		<article class="card">
			<header>
				<h3 class="card__title">{shop.name}</h3>
			</header>
			<ul>
				{#each shop.items as item}
				<li class="card-item">
					<svg class="card-item__icon card-item__icon--category">
					<title>Category icon</title>
					<use xlink:href="#shape-time"></use>
					</svg>
					<span class="card-item__text">{item}</span>
				</li>
				{/each}
			</ul>
		</article>
	{/each}
{/each}

<div class="grid-col-12">
	<p>Information correct on 20th April 2020.<br>
	Prepared by Royal Tunbridge Wells Together <a href="https://www.tunbridgewellstogether.co.uk" target="_blank" rel="noopener nofollow">
	tunbridgewellstogether.co.uk/</a></p>
</div>
