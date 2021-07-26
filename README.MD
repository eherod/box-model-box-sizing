# CSS Box Model and Box Sizing

***

In this post I will attempt to explain the CSS box model and the box-sizing property. I hope to convey the importance of conceptually grasping the box model early on in the process of learning CSS and web developement in general. 

***

I am a self taught (or perhaps more accurately, a self learning) web developer. Recently, I have been reflecting on my learning path and am beginning to recognize specific areas of importance that I did not initially give sufficient attention to when I first began learning web development. The box model is one example. 

Although I eventually came to fully understand the box model, I did so through a process of trial and error on the page. Only after I began to have a practical knowledge of how the box model worked (meaning that I could apply it) did I go back and gain a conceptual understanding. There is nothing wrong with this approach, however, I would have saved my self a lot of time and frustration had I simply set the time aside to learn the box model conceptually before attempting to build anything of significance. 

If you do not currently have a grasp on the box model but are able to mess around with the CSS until things fall into place, stop and spend some time to think about this topic conceptually. You can nail it down in 20 minutes and your productivity will take off respective to your current approach.

***

## The Box Model

***

The box model essentially defines the way an element is going to be displayed on the page. To fully grasp and attain control over the box model we need to focus only on 4 features: 
    
    Content

    Padding
    
    Border
    
    Margin

At the core of an element you have content. Around that content, space can be manipulated using padding. The space that is manipulated by padding is bounded by a border, and outside of that border, on all sides is your margin space.

### Content

Let's begin by looking closer at how content is handled by an HTML page in the browser. First, what do I mean by content? Content is anything that is contained within an element. For example, in the following h1 element:

```
<h1>Colorless green ideas sleep furiously</h1>
```

"Colorless green ideas sleep furiously" is the content of this element.

Likewise,

```
<p>Nothing I say is true</p>
```

"Nothing I say is true" is the content inside of the paragraph element.

Before any styles are added to your page, the content will be the main determining factor in how your element is displayed.<sup>*</sup> What do I mean by this? 

Consider the following: 

```
<p class="content-example"></p>
```

Notice that we have a paragraph tag with a class of "content-example" and there is no content inside of the paragraph tag. We can target "content-example" in our stylesheet like so:

```
.content-example{
    background: red; 
   
}

```

and assuming that the paragraph tag is the only element on our page, the result will be a blank page rather than a red box. 

Why is this? Because prior to adding any style manipulation to an element, the content is the determining factor for how your element is going to appear on the page. In this case we have a paragraph tag with no content and therefore we get nothing presented on the page. We can replace the paragraph tag with any other tag and the result will be the same. Consider this the next time you and add a background color to a div that has no content and no other styles applied to it. 


Let's put some content in our paragraph tag and have another look (keep in mind that I have styled this with a red background, as shown in the CSS block above).

```
<p>Now you see a red box stretching across the screen</p>
```




The content is typicaly manipulated using CSS properties like font-size, font-wieght, letter-spacing, color, ect.





(* 1) By default, the browser will have set margins and paddings on various elements so your first task when setting up your stylesheet is to turn these defaults off so that you have full control over the design of your page.  

