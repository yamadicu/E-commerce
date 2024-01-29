<script>
export default{
    name: 'MainComp',
}
</script>

<template>
    <body>
        <label id="summary">
            <input type="checkbox"/>
            <article>
                <div class="front">
                    <header>
                        <h2>Rosso Fermo</h2>
                        <span>29.90 €</span>
                    </header>
                    <img src="../../public/img/vino.png" alt="">
                    <h3>Marca Vino</h3>
                    <h4>Restanti: 13</h4>
                    <h4><a class="link" href="/">Prenota</a></h4>
                </div>
                <div class="back">
                    <header>
                        <h2>Rosso Fermo</h2>
                        <span>29.90 €</span>
                    </header>
                    <div>
                    <p>

                        In una giornata di sole radiante, il cielo azzurro si estendeva senza fine sopra la città, abbracciando i grattacieli che si stagliavano contro l'orizzonte. La vita urbana pulsava tra le strade trafficate, mentre le persone si affrettavano avanti e indietro, immerse nelle loro occupazioni quotidiane. I negozi sfoggiavano vetrine colorate, invitando i passanti a esplorare le ultime tendenze della moda e a gustare prelibatezze culinarie nei numerosi caffè e ristoranti che punteggiavano il paesaggio urbano.

                        Nei parchi, i raggi del sole filtravano attraverso le foglie degli alberi, creando un mosaico di ombre danzanti sulle aiuole fiorite. I bambini ridevano giocando nei parchi giochi, mentre gli adulti cercavano un momento di pace su una panchina, immersi nella lettura di un libro o semplicemente contemplando il mondo che li circondava. Gli uccelli cantavano in coro, contribuendo a creare una sinfonia armoniosa che accompagnava la tranquillità del momento.

                        Nelle strade più periferiche, la frenesia della vita quotidiana si attenuava, lasciando spazio a quartieri residenziali caratterizzati da case con giardini curati e strade alberate. Le famiglie si riunivano per pranzi all'aperto, con il profumo del barbecue nell'aria e il suono delle risate che risuonavano attraverso le case. I vicini si scambiavano saluti amichevoli mentre passeggiavano lungo le vie tranquille, creando un senso di comunità che andava al di là delle semplici mura domestiche.

                        Al di là della zona residenziale, la natura si manifestava in tutta la sua grandezza. Parchi nazionali e riserve naturali offrivano un rifugio per coloro che cercavano una pausa dalla vita frenetica della città. Sentieri serpeggiavano attraverso foreste secolari, conducendo a spettacolari cascate e viste panoramiche che toglievano il fiato. Gli amanti della natura esploravano questi luoghi, catturando la bellezza selvaggia del mondo in ogni passo.

                        Mentre il giorno lentamente cedeva il passo alla notte, le luci della città si accendevano, trasformando l'ambiente in un affascinante spettacolo di luci scintillanti. I ristoranti si riempivano di avventori, le strade si animavano di attività notturne e l'atmosfera vibrante della città non conosceva pausa. Gli edifici illuminati si ergevano maestosi, testimonianza della creatività e della determinazione umana nel plasmare il proprio ambiente.

                        In questa città in costante movimento, ogni giorno portava con sé nuove opportunità, esperienze e incontri. La vita, come un racconto avvincente, si svolgeva tra le sue strade, tessendo storie uniche e irripetibili per coloro che si immergevano in essa.
                    </p>
</div>
                </div>
            </article>
        </label>
        <!-- altre card -->
    </body>
    </template>

<style lang="scss" scoped>
body{
    font-family: "Poppins";

    article{
        position: relative;
        perspective: 1000px;
        width: 300px;
        height: 300px;
    }
    article Header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 40px;
        margin-bottom: 26px;
    }
    article .front, article .back{
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        text-align: center;
        backface-visibility: hidden;
        background: #ffffff;
        border-radius: 10px;
        padding: 24px;
        transition: 0.6s;
        cursor: pointer;
    }.back{
        transform: rotateY(180deg);
    }       
    
    .back div{
        max-height:15rem ;
        overflow: auto;
    }

    input{
        position: absolute;
        scale: 0;
    }

    input:checked ~ article .back{
        transform: rotateY(0);
    }

    input:checked ~ article .front{
        transform: rotateY(-180deg);
    }

    article var{
       line-height: 1;
    }

    article h3{
        margin: 0 0 10px;
        font-weight: 500;
    }

    h2,h3,h4{
        margin: 0;
        font-weight: 500;
    }

    a{
        text-decoration: none;
        color: black;
    }
}
</style>