---
title: "The Seven Restful Controller Actions on Laravel"
categories: [Laravel]
tags: [Laravel, Restful Controller, Controller Actions]
---

## The Seven Restful Controller Actions on Laravel

* Larabel Controller Actions Example

```php
<?php

namespace App\Http\Controllers;

use App\Article;

class ArticlesController extends Controller
{
    public function index()
    {
        // Render a list of a resource.

        $articles = Article::latest()->get();

        return view('articles.index', ['articles' => $articles]);
    }

    public function show($id)
    {
        // Show a single resource.

        $article = Article::find($id);

        return view('articles.show', ['article' => $article]);
    }

    public function create()
    {
        // Shows a view to create a new resource
    }

    public function store()
    {
        // Persist the new resource
    }

    public function edit()
    {
        // Show a view to edit an existing resource
    }

    public function update()
    {
        // Persist the edited resource
    }

    public function destroy()
    {
        // Delete the resource
    }
}
```

# References
---
Laravel From Scratch: The Seven Restful Controller Actions. Retrieved July 27, 2020, from <https://laracasts.com/series/laravel-6-from-scratch/episodes/21?autoplay=true>
---