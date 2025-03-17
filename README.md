# CenauScraper
https://www.ceneo.pl/84514582
##  Cenao scraping algorithmm
1. Analysis of the structure of the website
2. Send http requests to scrape data with reviews
3. Checking the response from the server
4. Parse the html code of the first page with reviews
5. Extract requiered data from the parsed code
6. Scrape other reviews (if there are more pages, move to the next page and repeat steps 2-6 for each of them)
7. Save extracted code

## Analysis of the structure of the webpage
| Component |Selector|Variable|
|-----------|--------|--------|
|opinion ID |.user-post user-post__card js_product-review | |
|author |.user-post__author-name | |
|recommendation |.user-post_author-name | |
|number of stars |.user-post__score-count | |
|content of opinion |.user-post__text | |
|list of advantages |.review-feature_item review-feauture_item--positive | |
|list of disadvantages |.review-feature_item review-feauture_item--negative | |
|for how many helpful |id^+votes-yes | |
|for how many unhelpful |id^+votes-no | |
|publishing date |.user-post__published | |
|purchase date | | |

##
<div class="user-post user-post__card js_product-review" data-entry-id="13551598">
<header class="user-post__header">
<div class="user-post__avatar user-rank__avatar lazyloaded" data-bg="/Content/img/account/avatar/0.svg" style="background-image: url(&quot;/Content/img/account/avatar/0.svg&quot;);"></div>
</header>
<div class="user-post__body">
<div class="user-post__content">

<span class="user-post__author-name">
b...a</span>

 <span class="user-post__author-recomendation">
 <em class="recommended">Polecam</em>
 </span>

<span class="user-post__score">
<span class="screen-reader-text">Ocena:</span>

<span class="score-container score-container--s  js_score-container ">
<span class="score-marker score-marker--s" style="width: 80.00%;"></span>
</span>



<span class="user-post__score-count">4/5</span>
 <span class="user-post__published">
Wystawiono
<time datetime="2020-12-10 19:41:04">5 lat temu, </time>
 <time datetime="2020-12-04 21:02:01">po 6 dniach</time> użytkowania  </span>

</span>

<div class="user-post__text">Wykonana dobrze, trochę za duża, z ledwością mieści mi się na biurku, ale może być. Drukuje ciszej w porównaniu z poprzednią drukarką HP 209a. Napełniłam tusze do pełna i po ok.10 kartkach ubyło mi 4 mm czarnego tuszu w pojemniku. Mam nadzieję, że będzie wydajna. Na razie nie mogę tego stwierdzić. Fajnie, że można zobaczyć, ile ubyło tuszu. Dolewanie jest banalnie proste, tusz nie wylewa się. Martwi mnie tylko, że przenosić trzeba ją w pozycji poziomej, bo inaczej tusz może się wylewać. Ogólnie jestem zadowolona z zakupu.</div>
 <div class="review-feature">
 <div class="review-feature__section">
<div class="review-feature__title">Zalety</div>
 <div class="review-feature__item review-feature__item--positive" data-new-icon="check">czyste napełnianie atramentem</div>
 <div class="review-feature__item review-feature__item--positive" data-new-icon="check">głośność pracy</div>
 </div>

 </div>



 <div class="review-pictures js_product-review-carousel" data-hide-controls="true">
 <div class="review-pictures__item js_product-image-miniature_el active">
<a class="js_gallery-trigger js_gallery-item js_gallery-anchor js_custom-click" data-elem-name="Gallery_users_pictures" href="//image.ceneostatic.pl/data/reviews/13551598/d70f68f3-7584-407a-8732-b78dfbb17ba1_r-hp-smart-tank-515-aio-1tj09a.jpg" data-type="img_user" data-index="0">
<img class="js_gallery-media js_review-product-thumb js_gallery-photo review-pictures__photo" loading="lazy" alt="HP Smart Tank 515 AiO (1TJ09A)" src="//image.ceneostatic.pl/data/reviews/13551598/d70f68f3-7584-407a-8732-b78dfbb17ba1_t-hp-smart-tank-515-aio-1tj09a.jpg" data-abuse-report-type="1" data-abuse-review-id="13551598" data-abuse-product-id="84514582">
</a>
</div>
 </div>

<div class="user-post__bottom">
 <span class="user-post__comments link link--accent">
 <a class="user-post__reply mr-0 link link--accent js_toggle-product-review-comments" href="#product-review-comments-13551598" rel="nofollow">Skomentuj opinię</a>
 </span>
 </div>
</div>
<div class="user-post__info">
<div class="d-flex align-items-center justify-content-end">
<div class="js_product-review-usefulness vote">
<button class="vote-yes js_product-review-vote js_vote-yes" data-new-icon="vote-up" data-url="SetOpinionVote" data-review-id="13551598" data-vote="1" data-voted="false" data-product-id="84514582" data-total-vote="2"><span id="votes-yes-13551598">2</span></button>
<button class="vote-no js_product-review-vote js_vote-no" data-new-icon="vote-down" data-url="SetOpinionVote" data-review-id="13551598" data-vote="0" data-voted="false" data-product-id="84514582" data-total-vote="3"><span id="votes-no-13551598">3</span></button>
</div>

<div class="dropdown-wrapper">
<span class="dots-icon-vert" data-toggle="dropdown"></span>
<ul class="dropdown-menu force-left">
<li class="dropdown-menu__item" data-product-id="84514582" data-review-id="13551598">


<div class="js_report-abuse report-abuse cursor-pointer" role="button" data-report-type="1">
<span>
Zgłoś </span>
</div>


</li>
</ul>
</div>
</div>

 <div class="review-pz" data-hint="Opinia została napisana przez Użytkownika, który kupił produkt.">
<em>Transakcja pochodzi z Marketplace Ceneo (usługi Kup Teraz).</em>
</div>


</div>


<div id="product-review-comments-13551598" class="js_product-review-comments js_product-review-hook js_product-review-comments-list hidden ">
<a class="user-post js_product-review-comment-toggle" href="#product-review-comment-13551598" data-product-review-id="84514582" data-review-id="13551598" data-comments-count="0" role="button">
<div class="user-post__header">
<div class="js_lazy user-post__avatar" data-bg="/Content/img/account/avatar/0.svg"></div>
</div>
<div class="user-post__body">
<div class="user-post__content">
<div class="user-post__text mt-0">
<textarea class="user-post__textarea user-post__textarea--dummy" placeholder="Wpisz swój komentarz"></textarea>
</div>
</div>
</div>
</a>
<div id="product-review-comment-13551598" class="js_product-review-form-hook"></div>
 </div>


</div>
</div>