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

Before any styles are added to your page, the content will be the main determining factor in how your element is displayed.

<sup>*By default, the browser will have set margins and paddings on various elements so your first task when setting up your stylesheet is to turn these defaults off so that you have full control over the design of your page.</sup>

 What do I mean by this? 

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

To see what this looks like in the browser follow this link:
https://silly-bell-afcd45.netlify.app/


You see that we now have our paragraph element displaying content and that content has a red background. I mentioned above that the content is the main determining factor in how your element is displayed on the screen, but it is not the only factor. You might expect that our red background would wrap tightly to the content in the paragraph tag and not extend beyond the last letter of the word "screen". However, we need to also consider how html handles elements. Elements in HTML are either displayed as block, inline, or inline-block. To remain within the scope of this article I will only touch briefly on this. 

Many of the common structural tags we use in HTML such as div, paragraph, header, and footer tags are by default block elements. A block element is assigned a block of space that stretches the width of its parent container. In our example above, the parent container of our paragraph element is the body element, which happens to also match the width of our viewport. So our paragraph element, being an html block element, stretches the width of the body element, and thus across the width of our viewport. 

Notice that the height of the red background barely stretches beyond the height of our content (Remember that the red color is distinct from and not to be confused as being a part of the content. Our content is what is placed between the opening and closing paragraph tags). The content is determining the height of the output we see on our screen. The content is typicaly manipulated using CSS properties like font-size, font-wieght, letter-spacing, color, ect.If you were to change the font-size of our paragraph element, the red background would grow or shrink in proportion to the newly assigned font-size. For design purposes, it is probably a good idea to have your font-family and font-size set up early on in the process of laying out your site because of the way changes to content can effect the other box model properties that we will soon discuss.

***

<center><h2>Padding</h2</center>

***

So far we have been discussing the core of our box model, that is, our element's content. Surrounding our content is padding. At the beginning of this article I mentioned that the space that can be manipulated by padding is bounded by a border. So, to understand how your element will respond when you add padding, remember that the padding will either expand or contract the space immediately surrounding your content, but it will not go beyond the element's border. In fact, when you apply padding to an element you are in effect pushing the element's border further away from the element's content. The space bewteen the content and the border is controlled with the padding property.

Let's return to our example paragraph element that we used in content section above.

```
<p>Now you see a red box stretching across the screen</p>
```

I am going to add 100px of padding to the left side of the paragraph element using the padding-left property: 

```
.content-example{
    background: red; 
    padding-left: 100px; 
}
```







 

