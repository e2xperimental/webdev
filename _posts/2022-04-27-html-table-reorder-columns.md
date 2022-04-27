---
layout: post
title: Reordering HTML Table columns with Javascript
date: 2022-04-27 11:00:00 -0000
category: Javascript
---

## Good

You don't lose your stake.

## Bad

You have to check if you won

You must claim prizes within 60 days.
Otherwise they will expire and you will not be able to claim them.

## Get Wallet

1. First, we get a list of all the tbody elements via

`mytablebody = document.getElementsByTagName("tbody")[0];`

Since there is only one tbody element in this example, this list will have only one item, which we retrieve by selecting the first element in that list using [0].

2. Next, we get all the `tr` elements that are descendants of the tbody

Note: Data Saver must be turned off.

[Source](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces)
[HTMLCollection.length](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection/length)
[Document.getElementsByTagName()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagName)
