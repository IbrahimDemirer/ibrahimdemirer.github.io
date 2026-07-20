---

title: "Talks"
layout: gridlay
sitemap: true
permalink: /talks/
---
## Talks

<div class="section-card">
  <h3>Locations</h3>
  <p>Selected locations of invited talks, workshops, and conference presentations. Click on a marker to view the event, year, and location.</p>

  <div id="talk-map" style="height: 520px; width: 100%; border-radius: 12px; margin-top: 1rem;"></div>
</div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css">

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var map = L.map("talk-map");

  L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
    maxZoom: 18,
    attribution: "&copy; OpenStreetMap contributors"
  }).addTo(map);

  var talks = [
    {
      title: "Post-Pandemic Economic Crises and Subjective Wellbeing: A Synthetic Control Analysis of Germany",
      event: "International Aging Gerontology & Geriatrics (IAGG)",
      date: "2026",
      location: "Amsterdam, Netherlands",
      lat: 52.3676,
      lng: 4.9041
    },
    {
      title: "Employment Trajectories and Mental Health Inequalities in Germany Before, During, and After the COVID-19 Pandemic: A Quasi-Experimental Panel Study",
      event: "Annual Conference of the European Consortium for Sociological Research",
      date: "2025",
      location: "Cologne, Germany",
      lat: 50.9375,
      lng: 6.9603
    },
    {
      title: "Bayes-Netzwerke, synthetische Daten und KI: Ein methodischer Rahmen für die prospektive Versorgungsplanung unter Hitzestress",
      event: "24th German Congress for Health Services Research",
      date: "2025",
      location: "Hamburg, Germany",
      lat: 53.5511,
      lng: 9.9937
    },
    {
      title: "Von der theoretisch besten zur praktisch besten Evidenz: ein Vorschlag für einen neuen evidenzbasierten Ansatz in der Gesundheitspolitik",
      event: "23rd German Congress for Health Services Research, State of the Art Session",
      date: "2024",
      location: "Potsdam, Germany",
      lat: 52.3906,
      lng: 13.0645
    },
    {
      title: "Case Causal Effects in Health Services Research?",
      event: "23rd German Congress for Health Services Research",
      date: "2024",
      location: "Potsdam, Germany",
      lat: 52.3906,
      lng: 13.0645
    },
    {
      title: "Sekundärdatenanalyse und kausale Inferenz",
      event: "DGMS Workshop",
      date: "2024",
      location: "Freiburg, Germany",
      lat: 47.9990,
      lng: 7.8421
    },
    {
      title: "Beispiele quasi-experimenteller Methoden in der Versorgungsforschung von Kindern und Jugendlichen",
      event: "Guest Lecture, University Hospital Düsseldorf",
      date: "2024",
      location: "Düsseldorf, Germany",
      lat: 51.2277,
      lng: 6.7735
    },
    {
      title: "Einfluss der COVID-19 Pandemie auf die hochaltrige Population in Deutschland",
      event: "Spring Conference of the DGS Sections Aging and Society & Medical and Health Sociology",
      date: "2024",
      location: "Dortmund, Germany",
      lat: 51.5136,
      lng: 7.4653
    },
    {
      title: "Von Umwelten und Kontexten: Konzeptionsversuche an der Schnittstelle zu methodenpluraler Forschung",
      event: "DGS Section Methods of Qualitative Social Research, SOFI Göttingen",
      date: "2024",
      location: "Göttingen, Germany",
      lat: 51.5413,
      lng: 9.9158
    },
    {
      title: "Berücksichtigung zeitveränderlicher Kontexte und Prozesse in der Outcome-Evaluation",
      event: "22nd German Congress for Health Services Research",
      date: "2023",
      location: "Berlin, Germany",
      lat: 52.5200,
      lng: 13.4050
    },
    {
      title: "Difference-in-Difference Erweiterung der mediational g-Formula zur Ermittlung der Auswirkungen der Covid-19 Pandemie auf bereits bestehende Prozesse gesundheitlicher Ungleichheiten",
      event: "Joint Congress of DGMS and DGMP",
      date: "2023",
      location: "Giessen, Germany",
      lat: 50.5841,
      lng: 8.6784
    },
    {
      title: "Modelling longitudinal processes in the face of the Covid-19 pandemic",
      event: "German Ageing Survey User Conference",
      date: "2023",
      location: "Berlin, Germany",
      lat: 52.5200,
      lng: 13.4050
    },
    {
      title: "Die Covid-19 Pandemie und gesundheitliche Ungleichheiten",
      event: "Poverty and Health Congress",
      date: "2023",
      location: "Berlin, Germany",
      lat: 52.5200,
      lng: 13.4050
    },
    {
      title: "Precarious employment and mental health during the Covid-19 pandemic. A longitudinal interacted mediation analysis",
      event: "RN21 Quantitative Methods Midterm Conference",
      date: "2022",
      location: "Salamanca, Spain",
      lat: 40.9701,
      lng: -5.6635
    },
    {
      title: "Neubewertung der Evaluation von Wirksamkeit in der Versorgungsforschung",
      event: "21st German Congress for Health Services Research",
      date: "2022",
      location: "Potsdam, Germany",
      lat: 52.3906,
      lng: 13.0645
    },
    {
      title: "Cooperation with University Hospital Cologne? Presentation of the Health Services Research Master Program and the IMVR",
      event: "Medical Venture Day",
      date: "2018",
      location: "Düsseldorf, Germany",
      lat: 51.2277,
      lng: 6.7735
    },
    {
      title: "Wer nicht fragt, fragt sich warum?",
      event: "Auf einen Kaffee mit der Wissenschaft, CORE-Net Citizen Event",
      date: "2018",
      location: "Cologne, Germany",
      lat: 50.9375,
      lng: 6.9603
    }
  ];

  var markers = L.featureGroup();

  talks.forEach(function (talk) {
    var marker = L.marker([talk.lat, talk.lng])
      .bindPopup(
        "<strong>" + talk.location + "</strong><br>" +
        "<em>" + talk.title + "</em><br>" +
        talk.event + "<br>" +
        talk.date
      );

    markers.addLayer(marker);
  });

  markers.addTo(map);

  map.fitBounds(markers.getBounds(), {
    padding: [40, 40]
  });
});
</script>

<div class="section-card">
  <h3>Invited Talks and Workshops</h3>

  <ul>
    <li><strong>Demirer, 2026.</strong> <em>Target Trial Emulation (TTE) mit Registerdaten.</em> Online discussion, Working Group Register Data, German Network for Health Services Research (DNVF).</li>

<li><strong>Demirer, 2024.</strong> <em>Von der theoretisch besten zur praktisch besten Evidenz: ein Vorschlag für einen neuen evidenzbasierten Ansatz in der Gesundheitspolitik.</em> State of the Art Session, 23rd German Congress for Health Services Research, Potsdam. Keynote co-speaker.</li>

<li><strong>Demirer, 2024.</strong> <em>Sekundärdatenanalyse und kausale Inferenz.</em> Workshop, German Society for Medical Sociology (DGMS) and University of Freiburg.</li>

<li><strong>Demirer, 2024.</strong> <em>Beispiele quasi-experimenteller Methoden in der Versorgungsforschung von Kindern und Jugendlichen.</em> Guest lecture, University Hospital Düsseldorf.</li>

  </ul>
</div>

<div class="section-card">
  <h3>Conference Presentations</h3>

  <ul>
    <li><strong>Demirer, 2026.</strong> <em>Post-Pandemic Economic Crises and Subjective Wellbeing: A Synthetic Control Analysis of Germany.</em> International Aging Gerontology & Geriatrics (IAGG), Amsterdam.</li>

<li><strong>Demirer, 2025.</strong> <em>Employment Trajectories and Mental Health Inequalities in Germany Before, During, and After the COVID-19 Pandemic: A Quasi-Experimental Panel Study.</em> Annual Conference of the European Consortium for Sociological Research, University of Cologne.</li>

<li><strong>Demirer, 2025.</strong> <em>Bayes-Netzwerke, synthetische Daten und KI: Ein methodischer Rahmen für die prospektive Versorgungsplanung unter Hitzestress.</em> 24th German Congress for Health Services Research, University Medical Center Hamburg-Eppendorf.</li>

<li><strong>Demirer, 2024.</strong> <em>Case Causal Effects in Health Services Research?</em> 23rd German Congress for Health Services Research, Potsdam.</li>

<li><strong>Demirer, 2024.</strong> <em>Einfluss der COVID-19 Pandemie auf die hochaltrige Population in Deutschland.</em> Spring Conference of the DGS Sections Aging and Society & Medical and Health Sociology, TU Dortmund.</li>

<li><strong>Demirer, 2024.</strong> <em>Von Umwelten und Kontexten: Konzeptionsversuche an der Schnittstelle zu methodenpluraler Forschung.</em> Conference “Heterogeneous Data – Plural Analyses: Challenges for Methodologically Plural Social Research”, DGS Section Methods of Qualitative Social Research and SOFI Göttingen.</li>

<li><strong>Demirer, 2023.</strong> <em>Berücksichtigung zeitveränderlicher Kontexte und Prozesse in der Outcome-Evaluation.</em> 22nd German Congress for Health Services Research, Berlin.</li>

<li><strong>Demirer, 2023.</strong> <em>Difference-in-Difference Erweiterung der mediational g-Formula zur Ermittlung der Auswirkungen der Covid-19 Pandemie auf bereits bestehende Prozesse gesundheitlicher Ungleichheiten.</em> Joint Congress of the German Society for Medical Sociology and the German Society for Medical Psychology, Giessen.</li>

<li><strong>Demirer, 2023.</strong> <em>Modelling longitudinal processes in the face of the Covid-19 pandemic.</em> German Ageing Survey User Conference, Berlin.</li>

<li><strong>Demirer, 2023.</strong> <em>Die Covid-19 Pandemie und gesundheitliche Ungleichheiten.</em> Poverty and Health Congress, Berlin.</li>

<li><strong>Demirer, 2022.</strong> <em>Precarious employment and mental health during the Covid-19 pandemic. A longitudinal interacted mediation analysis.</em> RN21 Quantitative Methods Midterm Conference, Salamanca.</li>

<li><strong>Demirer, 2022.</strong> <em>Neubewertung der Evaluation von Wirksamkeit in der Versorgungsforschung.</em> 21st German Congress for Health Services Research, Potsdam.</li>

<li><strong>Demirer, 2020.</strong> <em>Does positive affect mediate the effect of multimorbidity on depression?</em> Spring Conference of the DGS Section Methods of Empirical Social Research.</li>

<li><strong>Demirer, 2019.</strong> <em>Die Rolle des positiven Affektes im Kontext von Multimorbidität und Lebenszufriedenheit.</em> German Ageing Survey User Conference.</li>

  </ul>
</div>

<div class="section-card">
  <h3>Public Dissemination</h3>

  <ul>
    <li><strong>Demirer, 2018.</strong> <em>Cooperation with University Hospital Cologne? Presentation of the Health Services Research Master Program (M.Sc.) and the Institute of Medical Sociology, Health Services Research and Rehabilitation Science (IMVR).</em> Medical Venture Day, Düsseldorf.</li>

<li><strong>Demirer, 2018.</strong> <em>Wer nicht fragt, fragt sich warum?</em> “Auf einen Kaffee mit der Wissenschaft”, CORE-Net citizen event, Cologne.</li>

  </ul>
</div>
