
<!DOCTYPE html><html lang="en">
  <head><meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no"><title>Home - Lapis Re:LiGHTs English Fan Guide</title>

<meta name="description" content="Links to join the Lapis Re:LiGHTs fan communities, official sites, and pointers to other useful resources!">
<link rel="canonical" href="https://xeals.github.io/lapilai/"><link rel="alternate" type="application/rss+xml" title="Lapis Re:LiGHTs English Fan Guide" href="/lapilai/feed.xml"><!-- start favicons snippet, use https://realfavicongenerator.net/ --><link rel="apple-touch-icon" sizes="180x180" href="/lapilai/assets/apple-touch-icon.png"><link rel="icon" type="image/png" sizes="32x32" href="/lapilai/assets/favicon-32x32.png"><link rel="icon" type="image/png" sizes="16x16" href="/lapilai/assets/favicon-16x16.png"><link rel="manifest" href="/lapilai/assets/site.webmanifest"><link rel="mask-icon" href="/lapilai/assets/safari-pinned-tab.svg" color="#fc4d50"><link rel="shortcut icon" href="/lapilai/assets/favicon.ico">

<meta name="msapplication-TileColor" content="#ffc40d"><meta name="msapplication-config" content="/lapilai/assets/browserconfig.xml">

<meta name="theme-color" content="#e95098">
<!-- end favicons snippet -->
<link rel="stylesheet" href="/lapilai/assets/css/main.css"><link rel="stylesheet" href="https://cdn.bootcdn.net/ajax/libs/font-awesome/5.15.1/css/all.css" ><link rel="stylesheet" href="/lapilai/assets/types.css">

<style>
  figure {
      display: flex;
      flex-direction: column;
  }
  figure img {
      max-height: 200px;
      align-self: center;
  }
  figure figcaption {
      text-align: center;
  }

  figure img.large {
      max-height: 400px;
  }

  .item__image {
      align-self: center;
  }

  td > ul {
      margin-top: 0 !important;
      margin-bottom: 0 !important;
  }
</style>

<meta property="og:title"
    content="Home" />
<meta property="og:type" content="article" />
<meta property="og:url" content="https://xeals.github.io/lapilai/" />

<meta property="og:site_name" content="Lapis Re:LiGHTs English Fan Guide" />

<meta property="og:locale" content="en_AU" />


<meta property="og:image" content="https://xeals.github.io/lapilai/assets/og.png" />
<meta property="og:image:height" content="256" />
<meta property="og:image:width" content="256" />

<meta name="twitter:card"
    content="summary" />
<meta property="twitter:image" content="/assets/og.png" />


<meta property="og:description"
    content="Links to join the Lapis Re:LiGHTs fan communities, official sites, and pointers to other useful resources!" />


<meta name="theme-color" content="#e95098" />
<script>(function() {
  window.isArray = function(val) {
    return Object.prototype.toString.call(val) === '[object Array]';
  };
  window.isString = function(val) {
    return typeof val === 'string';
  };

  window.hasEvent = function(event) {
    return 'on'.concat(event) in window.document;
  };

  window.isOverallScroller = function(node) {
    return node === document.documentElement || node === document.body || node === window;
  };

  window.isFormElement = function(node) {
    var tagName = node.tagName;
    return tagName === 'INPUT' || tagName === 'SELECT' || tagName === 'TEXTAREA';
  };

  window.pageLoad = (function () {
    var loaded = false, cbs = [];
    window.addEventListener('load', function () {
      var i;
      loaded = true;
      if (cbs.length > 0) {
        for (i = 0; i < cbs.length; i++) {
          cbs[i]();
        }
      }
    });
    return {
      then: function(cb) {
        cb && (loaded ? cb() : (cbs.push(cb)));
      }
    };
  })();
})();
(function() {
  window.throttle = function(func, wait) {
    var args, result, thisArg, timeoutId, lastCalled = 0;

    function trailingCall() {
      lastCalled = new Date;
      timeoutId = null;
      result = func.apply(thisArg, args);
    }
    return function() {
      var now = new Date,
        remaining = wait - (now - lastCalled);

      args = arguments;
      thisArg = this;

      if (remaining <= 0) {
        clearTimeout(timeoutId);
        timeoutId = null;
        lastCalled = now;
        result = func.apply(thisArg, args);
      } else if (!timeoutId) {
        timeoutId = setTimeout(trailingCall, remaining);
      }
      return result;
    };
  };
})();
(function() {
  var Set = (function() {
    var add = function(item) {
      var i, data = this._data;
      for (i = 0; i < data.length; i++) {
        if (data[i] === item) {
          return;
        }
      }
      this.size ++;
      data.push(item);
      return data;
    };

    var Set = function(data) {
      this.size = 0;
      this._data = [];
      var i;
      if (data.length > 0) {
        for (i = 0; i < data.length; i++) {
          add.call(this, data[i]);
        }
      }
    };
    Set.prototype.add = add;
    Set.prototype.get = function(index) { return this._data[index]; };
    Set.prototype.has = function(item) {
      var i, data = this._data;
      for (i = 0; i < data.length; i++) {
        if (this.get(i) === item) {
          return true;
        }
      }
      return false;
    };
    Set.prototype.is = function(map) {
      if (map._data.length !== this._data.length) { return false; }
      var i, j, flag, tData = this._data, mData = map._data;
      for (i = 0; i < tData.length; i++) {
        for (flag = false, j = 0; j < mData.length; j++) {
          if (tData[i] === mData[j]) {
            flag = true;
            break;
          }
        }
        if (!flag) { return false; }
      }
      return true;
    };
    Set.prototype.values = function() {
      return this._data;
    };
    return Set;
  })();

  window.Lazyload = (function(doc) {
    var queue = {js: [], css: []}, sources = {js: {}, css: {}}, context = this;
    var createNode = function(name, attrs) {
      var node = doc.createElement(name), attr;
      for (attr in attrs) {
        if (attrs.hasOwnProperty(attr)) {
          node.setAttribute(attr, attrs[attr]);
        }
      }
      return node;
    };
    var end = function(type, url) {
      var s, q, qi, cbs, i, j, cur, val, flag;
      if (type === 'js' || type ==='css') {
        s = sources[type], q = queue[type];
        s[url] = true;
        for (i = 0; i < q.length; i++) {
          cur = q[i];
          if (cur.urls.has(url)) {
            qi = cur, val = qi.urls.values();
            qi && (cbs = qi.callbacks);
            for (flag = true, j = 0; j < val.length; j++) {
              cur = val[j];
              if (!s[cur]) {
                flag = false;
              }
            }
            if (flag && cbs && cbs.length > 0) {
              for (j = 0; j < cbs.length; j++) {
                cbs[j].call(context);
              }
              qi.load = true;
            }
          }
        }
      }
    };
    var load = function(type, urls, callback) {
      var s, q, qi, node, i, cur,
        _urls = typeof urls === 'string' ? new Set([urls]) : new Set(urls), val, url;
      if (type === 'js' || type ==='css') {
        s = sources[type], q = queue[type];
        for (i = 0; i < q.length; i++) {
          cur = q[i];
          if (_urls.is(cur.urls)) {
            qi = cur;
            break;
          }
        }
        val = _urls.values();
        if (qi) {
          callback && (qi.load || qi.callbacks.push(callback));
          callback && (qi.load && callback());
        } else {
          q.push({
            urls: _urls,
            callbacks: callback ? [callback] : [],
            load: false
          });
          for (i = 0; i < val.length; i++) {
            node = null, url = val[i];
            if (s[url] === undefined) {
              (type === 'js' ) && (node = createNode('script', { src: url }));
              (type === 'css') && (node = createNode('link', { rel: 'stylesheet', href: url }));
              if (node) {
                node.onload = (function(type, url) {
                  return function() {
                    end(type, url);
                  };
                })(type, url);
                (doc.head || doc.body).appendChild(node);
                s[url] = false;
              }
            }
          }
        }
      }
    };
    return {
      js: function(url, callback) {
        load('js', url, callback);
      },
      css: function(url, callback) {
        load('css', url, callback);
      }
    };
  })(this.document);
})();
</script><script>
  (function() {
    var TEXT_VARIABLES = {
      version: '2.2.6',
      sources: {
        font_awesome: 'https://cdn.bootcdn.net/ajax/libs/font-awesome/5.15.1/css/all.css',
        jquery: 'https://cdn.bootcss.com/jquery/3.1.1/jquery.min.js',
        leancloud_js_sdk: '//cdn.jsdelivr.net/npm/leancloud-storage@3.13.2/dist/av-min.js',
        chart: 'https://cdn.bootcss.com/Chart.js/2.7.2/Chart.bundle.min.js',
        gitalk: {
          js: 'https://cdn.bootcss.com/gitalk/1.2.2/gitalk.min.js',
          css: 'https://cdn.bootcss.com/gitalk/1.2.2/gitalk.min.css'
        },
        valine: 'https://unpkg.com/valine/dist/Valine.min.js',
        mathjax: 'https://cdn.bootcss.com/mathjax/2.7.4/MathJax.js?config=TeX-MML-AM_CHTML',
        mermaid: 'https://cdn.bootcss.com/mermaid/8.0.0-rc.8/mermaid.min.js'
      },
      site: {
        toc: {
          selectors: 'h1,h2,h3'
        }
      },
      paths: {
        search_js: '/lapilai/assets/search.js'
      }
    };
    window.TEXT_VARIABLES = TEXT_VARIABLES;
  })();
</script>
</head>
  <body>
    <div class="root" data-is-touch="false">
      <div class="layout--page js-page-root"><div class="page__main js-page-main page__viewport has-aside cell cell--auto">

      <div class="page__main-inner"><div class="page__header d-print-none"><header class="header"><div class="main">
      <div class="header__title">
        <div class="header__brand"><svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="24px" height="24px" viewBox="0 0 24 24">
<style type="text/css">
	.st0{fill:#515151;}
</style>
<path class="st0" d="M1.7,22.3c5.7-5.7,11.3-5.7,17,0c3.3-3.3,3.5-5.3,0.8-6c2.7,0.7,3.5-1.1,2.3-5.6s-3.3-5.2-6.3-2.1
	c3-3,2.3-5.2-2.1-6.3S7,1.8,7.7,4.6C7,1.8,5,2.1,1.7,5.3C7.3,11,7.3,16.7,1.7,22.3"/>
</svg>
<a title="Fan-made English documentation for helping new players navigating around Lapis Re:LiGHTs.
" href="/lapilai/">Lapis Re:LiGHTs English Fan Guide</a></div></div><nav class="navigation">
        <ul><li class="navigation__item"><a href="/lapilai/guide/faq">How to play</a></li><li class="navigation__item"><a href="/lapilai/content">Translated content</a></li><li class="navigation__item"><a href="/lapilai/tools">Tools</a></li><li class="navigation__item"><a href="/lapilai/card">Cards</a></li></ul>
      </nav></div>
  </header>
</div><div class="page__content"><div class ="main"><div class="grid grid--reverse">

              <div class="col-aside d-print-none js-col-aside"><aside class="page__aside js-page-aside"><div class="toc-aside js-toc-root"></div>
</aside></div>

              <div class="col-main cell cell--auto"><!-- start custom main top snippet -->

<!-- end custom main top snippet -->
<article itemscope itemtype="http://schema.org/WebPage"><header style="display:none;"><h1>Home</h1></header><meta itemprop="headline" content="Home"><div class="article__info clearfix"><ul class="right-col menu"></ul></div><meta itemprop="author" content="Your Name"/><div class="js-article-content"><div class="layout--home"></div>
<script>/*(function () {

})();*/
</script>

<p>Join us!</p>

<p><a href="https://discord.gg/MK9RDCG"><img src="https://badgen.net/discord/online-members/MK9RDCG" alt="Discord" /></a>
<a href="https://twitter.com/relightsEN"><img src="https://badgen.net/twitter/follow/relightsEN" alt="Twitter" /></a>
<a href="https://reddit.com/r/LapisReLights"><img src="https://badgen.net/reddit/subscribers/r/LapisReLights" alt="Reddit" /></a>
<!-- [![Fandom](https://badgen.net/badge/icon/fandom/pink?icon=chrome&label=Lapis+Re%3ALiGHTs+Wiki)](https://lapis-relights.fandom.com/wiki/Lapis_Re:Lights_Wiki) --></p>

<p>Official channels:</p>

<p><a href="https://www.lapisrelights.com"><img src="https://badgen.net/badge/icon/lapisrelights.com?icon=chrome&amp;label=official+site" alt="Official site" /></a>
<a href="https://twitter.com/lapisrelights"><img src="https://badgen.net/twitter/follow/lapisrelights" alt="Official Twitter" /></a>
<a href="https://twitter.com/lapi_staff"><img src="https://badgen.net/twitter/follow/lapi_staff" alt="Official game Twitter" /></a>
<a href="https://www.youtube.com/channel/UCbia-gfyNViX55iSBIP5M4Q"><img src="https://badgen.net/badge/icon/YouTube/red?icon=peertube&amp;label=ラピスリライツ公式チャンネル" alt="Official YouTube" /></a></p>

<p>Other useful guides:</p>

<ul>
  <li><a href="https://docs.google.com/document/d/1-O9O_rimeYmnmiHeOz1Nv0c18emhucS2PDt5MMgTQxc">Card skills</a></li>
  <li><a href="https://docs.google.com/document/d/1-eponAh9YcRvWfUJBClvhbDotbv0cSnuXYh4sf4VvrA">Unit skills</a></li>
</ul>

<h2 id="contribute">Contribute</h2>

<p>We are always welcome to contributors! If you find some of the documentation or
translations incorrect or wish to help clarify some explanations, please feel
free to reach out on the fan Discord server above, or contribute directly on
<a href="https://github.com/xeals/lapilai">GitHub</a>. We also welcome people providing
translations to non-English languages!</p>

<h2 id="support-or-contact">Support or contact</h2>

<p>Reach out to @xeal on <a href="https://discordapp.com/users/196091333658542080">Discord</a>
or <a href="https://github.com/xeals">Github</a>.</p>


</div><section class="page__comments d-print-none"></section></article><!-- start custom main bottom snippet -->

<!-- end custom main bottom snippet -->
</div>
            </div></div></div><div class="page__footer d-print-none"><footer class="footer py-4 js-page-footer">
  <div class="main"><div itemscope itemtype="http://schema.org/Person">
      <meta itemprop="name" content="Your Name"><meta itemprop="url" content="/lapilai/"><meta itemprop="description" content="I am an amazing person."><div class="footer__author-links"><div class="author-links">
  <ul class="menu menu--nowrap menu--inline"></ul>
</div>
</div>
    </div><div class="site-info mt-2">
      <div>This site is not representitive of and is not associated
with <a href="https://lapisrelights.com">Lapis Re:LIGHTs</a>.  Lapis Re:LiGHTs
is © KLabGames and KADOKAWA CORPORATION 2017-2021. All logos, images, and game
content used in this site are Trademarks of the aforementioned entities.
<br>
Site content is provided by the Lapis Re:LiGHTs English Fan Discord Server
        contributors 2021.
        Powered by <a title="Jekyll is a simple, blog-aware, static site generator."
          href="http://jekyllrb.com/">Jekyll</a> & <a title="TeXt is a super customizable Jekyll theme."
          href="https://github.com/kitian616/jekyll-TeXt-theme">TeXt Theme</a>.
      </div>
    </div>
  </div>
</footer>
</div></div>
    </div><script>(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    var $body = $('body'), $window = $(window);
    var $pageRoot = $('.js-page-root'), $pageMain = $('.js-page-main');
    var activeCount = 0;
    function modal(options) {
      var $root = this, visible, onChange, hideWhenWindowScroll = false;
      var scrollTop;
      function setOptions(options) {
        var _options = options || {};
        visible = _options.initialVisible === undefined ? false : show;
        onChange = _options.onChange;
        hideWhenWindowScroll = _options.hideWhenWindowScroll;
      }
      function init() {
        setState(visible);
      }
      function setState(isShow) {
        if (isShow === visible) {
          return;
        }
        visible = isShow;
        if (visible) {
          activeCount++;
          scrollTop = $(window).scrollTop() || $pageMain.scrollTop();
          $root.addClass('modal--show');
          $pageMain.scrollTop(scrollTop);
          activeCount === 1 && ($pageRoot.addClass('show-modal'), $body.addClass('of-hidden'));
          hideWhenWindowScroll && window.hasEvent('touchstart') && $window.on('scroll', hide);
          $window.on('keyup', handleKeyup);
        } else {
          activeCount > 0 && activeCount--;
          $root.removeClass('modal--show');
          $window.scrollTop(scrollTop);
          activeCount === 0 && ($pageRoot.removeClass('show-modal'), $body.removeClass('of-hidden'));
          hideWhenWindowScroll && window.hasEvent('touchstart') && $window.off('scroll', hide);
          $window.off('keyup', handleKeyup);
        }
        onChange && onChange(visible);
      }
      function show() {
        setState(true);
      }
      function hide() {
        setState(false);
      }
      function handleKeyup(e) {
        // Char Code: 27  ESC
        if (e.which ===  27) {
          hide();
        }
      }
      setOptions(options);
      init();
      return {
        show: show,
        hide: hide,
        $el: $root
      };
    }
    $.fn.modal = modal;
  });
})();
</script><div class="modal modal--overflow page__search-modal d-print-none js-page-search-modal"></div></div>


<script>(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    function scrollToAnchor(anchor, duration, callback) {
      var $root = this;
      $root.animate({ scrollTop: $(anchor).position().top }, duration, function() {
        window.history.replaceState(null, '', window.location.href.split('#')[0] + anchor);
        callback && callback();
      });
    }
    $.fn.scrollToAnchor = scrollToAnchor;
  });
})();
(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    function affix(options) {
      var $root = this, $window = $(window), $scrollTarget, $scroll,
        offsetBottom = 0, scrollTarget = window, scroll = window.document, disabled = false, isOverallScroller = true,
        rootTop, rootLeft, rootHeight, scrollBottom, rootBottomTop,
        hasInit = false, curState;

      function setOptions(options) {
        var _options = options || {};
        _options.offsetBottom && (offsetBottom = _options.offsetBottom);
        _options.scrollTarget && (scrollTarget = _options.scrollTarget);
        _options.scroll && (scroll = _options.scroll);
        _options.disabled !== undefined && (disabled = _options.disabled);
        $scrollTarget = $(scrollTarget);
        isOverallScroller = window.isOverallScroller($scrollTarget[0]);
        $scroll = $(scroll);
      }
      function preCalc() {
        top();
        rootHeight = $root.outerHeight();
        rootTop = $root.offset().top + (isOverallScroller ? 0 :  $scrollTarget.scrollTop());
        rootLeft = $root.offset().left;
      }
      function calc(needPreCalc) {
        needPreCalc && preCalc();
        scrollBottom = $scroll.outerHeight() - offsetBottom - rootHeight;
        rootBottomTop = scrollBottom - rootTop;
      }
      function top() {
        if (curState !== 'top') {
          $root.removeClass('fixed').css({
            left: 0,
            top: 0
          });
          curState = 'top';
        }
      }
      function fixed() {
        if (curState !== 'fixed') {
          $root.addClass('fixed').css({
            left: rootLeft + 'px',
            top: 0
          });
          curState = 'fixed';
        }
      }
      function bottom() {
        if (curState !== 'bottom') {
          $root.removeClass('fixed').css({
            left: 0,
            top: rootBottomTop + 'px'
          });
          curState = 'bottom';
        }
      }
      function setState() {
        var scrollTop = $scrollTarget.scrollTop();
        if (scrollTop >= rootTop && scrollTop <= scrollBottom) {
          fixed();
        } else if (scrollTop < rootTop) {
          top();
        } else {
          bottom();
        }
      }
      function init() {
        if(!hasInit) {
          var interval, timeout;
          calc(true); setState();
          // run calc every 100 millisecond
          interval = setInterval(function() {
            calc();
          }, 100);
          timeout = setTimeout(function() {
            clearInterval(interval);
          }, 45000);
          window.pageLoad.then(function() {
            setTimeout(function() {
              clearInterval(interval);
              clearTimeout(timeout);
            }, 3000);
          });
          $scrollTarget.on('scroll', function() {
            disabled || setState();
          });
          $window.on('resize', function() {
            disabled || (calc(true), setState());
          });
          hasInit = true;
        }
      }

      setOptions(options);
      if (!disabled) {
        init();
      }
      $window.on('resize', window.throttle(function() {
        init();
      }, 200));
      return {
        setOptions: setOptions,
        refresh: function() {
          calc(true, { animation: false }); setState();
        }
      };
    }
    $.fn.affix = affix;
  });
})();
(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    function toc(options) {
      var $root = this, $window = $(window), $scrollTarget, $scroller, $tocUl = $('<ul class="toc toc--ellipsis"></ul>'), $tocLi, $headings, $activeLast, $activeCur,
        selectors = 'h1,h2,h3', container = 'body', scrollTarget = window, scroller = 'html, body', disabled = false,
        headingsPos, scrolling = false, hasRendered = false, hasInit = false;

      function setOptions(options) {
        var _options = options || {};
        _options.selectors && (selectors = _options.selectors);
        _options.container && (container = _options.container);
        _options.scrollTarget && (scrollTarget = _options.scrollTarget);
        _options.scroller && (scroller = _options.scroller);
        _options.disabled !== undefined && (disabled = _options.disabled);
        $headings = $(container).find(selectors).filter('[id]');
        $scrollTarget = $(scrollTarget);
        $scroller = $(scroller);
      }
      function calc() {
        headingsPos = [];
        $headings.each(function() {
          headingsPos.push(Math.floor($(this).position().top));
        });
      }
      function setState(element, disabled) {
        var scrollTop = $scrollTarget.scrollTop(), i;
        if (disabled || !headingsPos || headingsPos.length < 1) { return; }
        if (element) {
          $activeCur = element;
        } else {
          for (i = 0; i < headingsPos.length; i++) {
            if (scrollTop >= headingsPos[i]) {
              $activeCur = $tocLi.eq(i);
            } else {
              $activeCur || ($activeCur = $tocLi.eq(i));
              break;
            }
          }
        }
        $activeLast && $activeLast.removeClass('active');
        ($activeLast = $activeCur).addClass('active');
      }
      function render() {
        if(!hasRendered) {
          $root.append($tocUl);
          $headings.each(function() {
            var $this = $(this);
            $tocUl.append($('<li></li>').addClass('toc-' + $this.prop('tagName').toLowerCase())
              .append($('<a></a>').text($this.text()).attr('href', '#' + $this.prop('id'))));
          });
          $tocLi = $tocUl.children('li');
          $tocUl.on('click', 'a', function(e) {
            e.preventDefault();
            var $this = $(this);
            scrolling = true;
            setState($this.parent());
            $scroller.scrollToAnchor($this.attr('href'), 400, function() {
              scrolling = false;
            });
          });
        }
        hasRendered = true;
      }
      function init() {
        var interval, timeout;
        if(!hasInit) {
          render(); calc(); setState(null, scrolling);
          // run calc every 100 millisecond
          interval = setInterval(function() {
            calc();
          }, 100);
          timeout = setTimeout(function() {
            clearInterval(interval);
          }, 45000);
          window.pageLoad.then(function() {
            setTimeout(function() {
              clearInterval(interval);
              clearTimeout(timeout);
            }, 3000);
          });
          $scrollTarget.on('scroll', function() {
            disabled || setState(null, scrolling);
          });
          $window.on('resize', window.throttle(function() {
            if (!disabled) {
              render(); calc(); setState(null, scrolling);
            }
          }, 100));
        }
        hasInit = true;
      }

      setOptions(options);
      if (!disabled) {
        init();
      }
      $window.on('resize', window.throttle(function() {
        init();
      }, 200));
      return {
        setOptions: setOptions
      };
    }
    $.fn.toc = toc;
  });
})();
/*(function () {

})();*/
</script><script>
  /* toc must before affix, since affix need to konw toc' height. */(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  var TOC_SELECTOR = window.TEXT_VARIABLES.site.toc.selectors;
  window.Lazyload.js(SOURCES.jquery, function() {
    var $window = $(window);
    var $articleContent = $('.js-article-content');
    var $tocRoot = $('.js-toc-root'), $col2 = $('.js-col-aside');
    var toc;
    var tocDisabled = false;
    var hasSidebar = $('.js-page-root').hasClass('layout--page--sidebar');
    var hasToc = $articleContent.find(TOC_SELECTOR).length > 0;

    function disabled() {
      return $col2.css('display') === 'none' || !hasToc;
    }

    tocDisabled = disabled();

    toc = $tocRoot.toc({
      selectors: TOC_SELECTOR,
      container: $articleContent,
      scrollTarget: hasSidebar ? '.js-page-main' : null,
      scroller: hasSidebar ? '.js-page-main' : null,
      disabled: tocDisabled
    });

    $window.on('resize', window.throttle(function() {
      tocDisabled = disabled();
      toc && toc.setOptions({
        disabled: tocDisabled
      });
    }, 100));

  });
})();
(function() {
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    var $window = $(window), $pageFooter = $('.js-page-footer');
    var $pageAside = $('.js-page-aside');
    var affix;
    var tocDisabled = false;
    var hasSidebar = $('.js-page-root').hasClass('layout--page--sidebar');

    affix = $pageAside.affix({
      offsetBottom: $pageFooter.outerHeight(),
      scrollTarget: hasSidebar ? '.js-page-main' : null,
      scroller: hasSidebar ? '.js-page-main' : null,
      scroll: hasSidebar ? $('.js-page-main').children() : null,
      disabled: tocDisabled
    });

    $window.on('resize', window.throttle(function() {
      affix && affix.setOptions({
        disabled: tocDisabled
      });
    }, 100));

    window.pageAsideAffix = affix;
  });
})();
</script>
    </div>
    <script>(function () {
  var $root = document.getElementsByClassName('root')[0];
  if (window.hasEvent('touchstart')) {
    $root.dataset.isTouch = true;
    document.addEventListener('touchstart', function(){}, false);
  }
})();
</script>
  </body>
</html>

