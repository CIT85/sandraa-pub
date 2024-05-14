# Project Topic
## Exploring Mindfulness as a self-care practice:
- At first I thought about picking something book related but as finals are approaching I started thinking about self-care. Unless it's something that we take into consideration and actively think about self-care isn't always a priority especially when there are deadlines and responsibilities of school and work. Self-care is usally thought of as something that we do for ourselves such as time alone, time to relax or perhaps take a bubble bath. Mindfulness practiced as self-care can spread into health both physical and emotional both which then in turn feed into self-care. Mindfulness is not something that stays stagnent on its own but spread to other things. I used CHATgpt to search topics of self-care and mindfulness then started to use teh results to tailor my focus. I worked backwords a little and started asking CHATgpt to define "Mindfulness" and then "self-care". In order to understand the terms I searched "Mindfulness as a self-care tool", "Mindfulness vs Self-Care","mindfulness as a topic of interest" just different ways to see how Mindfulness and self-care relate. 
- The three things that caught my eye:
    1. **Emotional Regulation:** Mindfulness helps individuals become more aware of their emotions without judgment. By practicing mindfulness, people can observe their emotions as they arise, allowing them to respond to them in a healthy and constructive manner. This emotional awareness and regulation are fundamental aspects of self-care, as it enables individuals to manage stress, anxiety, and other negative emotions effectively.
    2. **Better Physical Health:** Mindfulness has been associated with various physical health benefits, including improved sleep quality, reduced inflammation, and enhanced immune function. By practicing mindfulness, individuals can support their physical well-being, which is an essential aspect of self-care. Additionally, mindfulness-based interventions have been shown to complement medical treatments for conditions such as chronic pain and cardiovascular disease, further highlighting the role of mindfulness in holistic self-care.
    3. **Use Mindfulness in Daily Activities:** Infuse mindfulness into your daily activities by bringing awareness to the present moment. Whether you're washing dishes, walking to work, or having a conversation, try to engage fully in the activity without getting lost in thoughts or distractions. Pay attention to your senses, thoughts, and emotions as they arise, without judgment.
        - **Start with Simple Practices:** Begin by incorporating simple mindfulness practices into your daily routine. This could include mindful breathing exercises, where you focus on your breath for a few minutes to anchor yourself in the present moment. You can also try mindful walking, eating, or body scans to cultivate awareness in different aspects of your life.
### Menu - initial
1. Home
2. Understanding the Emotional Importance
    - Emotions
3. Health Benefits
    - Health
4. Implmentation
    - Implementation
### Menu - Current as of P3
1. Home (main page with overview of the content for each individual page, all except sitemap and Group)
2. Understanding the Emotional Importance
    - Emotions (3 sections)
3. Health Benefits
    - Health (3 sections)
4. Implmentation
    - Implementation (4 sections)
        - Group (this is the subpage within a subpage)
- Sitemap (includes color pallete and brief about Group)
### p3

- header, h1, h2, h3
    - Used align to show off each section
    - sticky: each h2 sections off each portion about that header
    - this part was tricky, I know what I wanted to see but wasn't too confident on how to make it happen. Switching betweenviewing the actual page and the code I was able to make the code reflect what I wanted to see on the page.
- paragraphs
    - center aligned to fall under the header or h they are under
    - used flex to move the placement of the paragraphs
- images
    - centered along with figcaption, figcaption credits Bing for image generation
    - images optimized by making them either equal to the sizing in the html or slightly bigger due to being shared on multiple pages

- table
    - centered with it's content, applied to both tables in Index and Implementation
        - **entered classes within html to maniputlate paragraphs, images and the table in css**
- lists
    - come lists have been centered
### p3 part 2
- Flex 
    - flex was modified but still needs adjusting to be true flex
- Media Queries
    - Sample media query
    - '@media (max-width: 576px) {
            .menu-ul {
                display: flex;
                flex-direction: column !important;
                align-items: center;
                list-style-position: inside;
            }}'
        - I started with this media query but changed it to apply text color and back-ground color changes to reflect the differnet window sizes.
        - Attempted but failed to change the layout of the menu links, they should change from row to column as the page shrinks in display size
        - Went back to edit queries and was able to get the colors working as well as image resizing and text. Menu change from row to column still and issue.

### Final
- all links have been updated
    - Contact me link has been added to the Sitemap footer
    - all page links have been listed in the Sitemap
- contact me page has been added
    - site includes a picture and full form
- all pages have been validated and the HTML5 Outliner has been checked