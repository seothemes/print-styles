# Print Styles

Basic CSS print styles for WordPress themes.

```css
@media print {

	*,
	*:before,
	*:after {
		color: #333 !important;
		background: transparent !important;
		box-shadow: none !important;
		text-shadow: none !important;
	}

	a,
	a:visited {
		text-decoration: underline;
	}

	a[href]:after {
		content: " (" attr(href) ")";
	}

	abbr[title]:after {
		content: " (" attr(title) ")";
	}

	a[href^="javascript:"]:after,
	a[href^="#"]:after,
	.site-title > a:after {
		content: "";
	}

	thead {
		display: table-header-group;
	}

	img,
	tr {
		page-break-inside: avoid;
	}

	img {
		max-width: 100% !important;
	}

	@page {
		margin: 2cm 0.5cm;
	}

	p,
	h2,
	h3 {
		orphans: 3;
		widows: 3;
	}

	blockquote,
	pre {
		border: 1px solid #999;
		page-break-inside: avoid;
	}

	.content,
	.content-sidebar {
		width: 100%;
	}

	button,
	input,
	select,
	textarea,
	.breadcrumb,
	.comment-edit-link,
	.comment-form,
	.comment-list .reply a,
	.comment-reply-title,
	.edit-link,
	.entry-comments-link,
	.entry-footer,
	.genesis-box,
	.header-widget-area,
	.hidden-print,
	.home-top,
	.nav-primary,
	.nav-secondary,
	.post-edit-link,
	.sidebar {
		display: none !important;
	}

	.title-area {
		width: 100%;
		text-align: center;
	}

	.site-title > a {
		margin: 0;
		text-decoration: none;
		text-indent: 0;
	}

	.site-inner {
		position: relative;
		top: -100px;
		padding-top: 0;
	}

	.author-box {
		margin-bottom: 0;
	}

	h1,
	h2,
	h3,
	h4,
	h5,
	h6 {
		orphans: 3;
		page-break-after: avoid;
		page-break-inside: avoid;
		widows: 3;
	}

	img {
		page-break-after: avoid;
		page-break-inside: avoid;
	}

	blockquote,
	pre,
	table {
		page-break-inside: avoid;
	}

	dl,
	ol,
	ul {
		page-break-before: avoid;
	}
}
```