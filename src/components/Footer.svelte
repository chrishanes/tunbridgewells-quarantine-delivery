<script>
    function clickEvent(name) {
        gtag('event', 'click', { 'event_category': name, 'event_label': 'Website' })
    }
</script>

<style>
    .footer-wrapper {
        margin: 20px 10px;
    }
    .footer {
		margin: 20px 0;
        display: flex;
        flex-direction: column;
    }

    @media (min-width: 768px) {
		.footer-wrapper {
            margin: 20px 16px;
        }
        .footer {
            flex-direction: row;
            justify-content: space-between;
		}
    }
    
    .footer-item {
        font-size: 1.4rem;
        color: var(--blue);
    }

    .footer-item a:hover {
        color: var(--gold);
    }
</style>

<footer class="footer-wrapper">
    <ul class="footer">
        <li class="footer-item">Website by <a href="http://chrishanes.co.uk/" target="_blank" rel="noopener nofollow" on:click={() => clickEvent("Chris Hanes")}>Chris Hanes</a></li>
        <li class="footer-item">Add your listing 
            <a href="https://docs.google.com/forms/d/1u6KEhqYW2_QjlRKs2CvrGTzLa_QRbK4TjDxOBDFVMvE" rel="noopener nofollow" target="_blank">
                here
            </a>
        </li>
        <li class="footer-item">Visit the 
            <a href="https://www.facebook.com/groups/243897146788661/" target="_blank" aria-label="Visit the Facebook group" rel="noopener nofollow">
                Facebook Group
            </a>
        </li>
    </ul>
</footer>