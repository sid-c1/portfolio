<script lang="ts">
    import map from '$lib/map viewer.png';
    import directory from '$lib/company directory.png';
</script>

<main>
    <section id="home" class="min-h-screen p-15 text-2xl text-center flex flex-col items-center justify-center">
        <div>
            Welcome to my portfolio! I am a
            <strong> UK based Software Engineer</strong>
            specialising in
            <strong> Full Stack Web Development</strong>.
        </div>
        <div class="min-w-max h-40"></div>
        <div class="p-15 text-xl text-center text-[#ccc6b4]">
            <strong>
                I am currently available for employment. <br>
                If you are hiring, please use the contact form and I'll get back to you as soon as possible.
            </strong>
        </div>
    </section>

    <section id="projects" class="min-h-screen p-20">
        <h5>
            <a class="text-2xl" href="https://medianon.org" target="_blank">
                medianon
            </a>
        </h5>
        <p>
            A free and open source anonymous forum. <br>
            Users can make a custom board or use a public board. <br>
            Posts are automatically archived and deleted. <br>
            No registration, cookies or tracking. <br><br>
            <a href="https://github.com/medianon/medianon" target="_blank">GitHub link</a> <br><br>
            Uses: <br>
            SvelteKit, Tailwind, Firebase, Vercel

        </p><br><br>
        <h5>
            <a class="text-2xl" href="https://mapviewer.page.gd" target="_blank">
                Gazetteer
            </a>
        </h5>
        <img src={map} alt="Gazetteer">
        <p>
            An interactive map to learn about countries.<br>
            Fetches data from multiple APIs.<br><br>
            Uses: <br>
            HTML/CSS/JS, jQuery, PHP <br>
            <a href="https://leafletjs.com">Leaflet JS</a> <br>
            <a href="https://api-ninjas.com">API Ninjas</a> <br>
            <a href="https://www.geonames.org">GeoNames</a> <br>
            <a href="https://www.weatherapi.com">WeatherAPI</a> <br>
            <a href="https://openexchangerates.org">Open Exchange Rates</a> <br>
            <a href="https://worldnewsapi.com">World News API</a> <br>
            <a href="https://www.vantilburger.com">VanTilburger</a> <br>
        </p> <br><br>
        <h5>
            <a class="text-2xl" href="https://companydirectory.free.nf" target="_blank">
                Company Directory
            </a>
        </h5>
        <img src={directory} alt="Company Directory">
        <p>
            A CRUD application to manage an SQL database. <br>
            Consist of three tables: personnel, department and location. <br>
            Search and filter options to make navigation easier. <br><br>
            Uses: <br>
            HTML/CSS/JS, jQuery, PHP, SQL
        </p> <br><br>
        <h5>
            <a class="text-2xl" href="https://geonamesexample.rf.gd" target="_blank">
                GeoNames API Examples
            </a>
        </h5>
        <p>
            A simple exercise to get familiar with API usage. <br>
            The first table gets the required inputs from the user. <br>
            A second table displays the returned data. <br><br>
            <a href="https://github.com/sid-c1/API-examples">GitHub link</a><br><br>
            Uses: <br>
            HTML, JS, PHP <br>
            <a href="https://www.geonames.org">GeoNames</a>
        </p>
    </section>

    <section id="skills" class="min-h-screen p-10 text-center">
        <h3><br>
            HTML - CSS - JS <br>
            SvelteKit - Tailwind CSS - Firebase
        </h3><br>
        <h3>
            Python, C#, Java, PHP <br>
            Flutterflow, SQL/NoSQL, Git
        </h3><br>
        <strong class="text-xl text-[#ccc6b4]">
            I am always happy to learn new technologies. Everything listed above was new to me at one point.
        </strong><br><br><br>

        <h3>
            <u>
                Experience
            </u>
        </h3>
        <h5>
            Document Control and IT Management (2022-2023) - <em>NT Killingley</em>
        </h5><br>
    
        <br><br><h3>
            <u>
                Education
            </u>
        </h3>
        BSc in Computer Science with Honours (2:1) - <em>Coventry University</em>
    </section>

    <section id="contact" class="min-h-screen p-10 ml-3">
        <div>
            <form action="https://formsubmit.co/c54003805695bd527f62d07c49094118" method="POST">
                <fieldset class="grid">
                    <label>
                        Name
                        <input type="text" name="name" required placeholder="Enter name">
                    </label>
                    <label>
                        Email
                        <input type="email" name="email" required placeholder="Enter email">
                    </label>
                </fieldset>
                <textarea name="message" placeholder="Enter message"></textarea> <br>
                <div class="p-10">
                    <button type="submit">Send</button>
                </div>
            </form>
        </div>
    </section>
</main>