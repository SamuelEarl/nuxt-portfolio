<template>
  <Layout>
    <h1>Recent Projects</h1>

    <!-- <p>(Describe the stack that is used [e.g. Vue.js, Vue Router, Vuex, D3.js, serverless functions, Neo4j, GraphQL] and the features along with GIFs showing those features.)</p> -->

    <div class="content">
      <h2>Real-time Data Dashboard</h2>

      <p>I did some work for a large manufacturing company that needed a second-by-second data dashboard. This app provides real-time status updates on various stations and equipment throughout the manufacturing facility. The front-end is a single-page application (SPA) written with Vue.js, Vue Router, and Vuex. All the UI components are custom made and the entire app (including the navigation and all the various windows) is completely mobile-responsive.</p>

      <p><strong>These are some of the features in this app:</strong></p>

      <h3>Real-time Data Via WebSockets</h3>
      <img alt="Real-time data" src="~/assets/img/real-time-data-via-websockets.gif" class="data-dashboard-image" />
      <p class="caption">The data from the back-end is fed to the UI and inserted into a real-time dashboard that includes summary data and live charts.</p>

      <h3>Interactive Charts With D3.js</h3>
      <img alt="Interactive charts" src="~/assets/img/interactive-charts.gif" class="data-dashboard-image" />
      <p class="caption">These charts were custom created using D3.js. Users can change the data ranges that they want displayed for each chart. Also, when a user hovers over a data point, the data for that specific point is displayed.</p>

      <h3>Record And Download Data Without Servers</h3>
      <img alt="Record and download data" src="~/assets/img/record-and-download-data.gif" class="data-dashboard-image" />
      <p class="caption">Users can record data and download the recorded data as a CSV file for further analysis. The downloaded CSV file is saved to the user's computer. The data recording and downloading feature is completely implemented in the browser (i.e. no server-side code involved). See <a href="/code-samples#record-download-data">my first code sample</a> for a working example that you can try yourself.</p>

      <h3>Collapsible Side Panel With Auto-adjusting Charts</h3>
      <img alt="Auto-adjusting charts" src="~/assets/img/auto-adjusting-charts.gif" class="data-dashboard-image" />
      <p class="caption">This feature allows users to get a larger view of the charts for a more detailed view. The real magic is that the charts auto-adjust their size to fit the available space.</p>


      <p><em><strong>NOTE:</strong> I wrote the original back-end server in Node.js with MongoDB and WebSockets. However, after working on the project for a while, our team realized that Go would be a better fit for what we needed.</em></p>
    </div>

    <div class="content">
      <h2>Budget App</h2>

      <p>This app uses Vue.js, serverless functions, and Neo4j (because I love graph databases &mdash; Neo4j in particular). I placed a high priority on security (explained below) and spent a lot of time working on the UX (with a lot of user feedback from my wife).</p>

      <p><strong>These are some of the features in this app:</strong></p>
      <h3>Responsive Design and PWA</h3>
      <div class="budget-app-images">
        <img alt="Budget app mobile 1" src="~/assets/img/budget-app-mobile-1.png" class="budget-app-phone" />
        <img alt="Budget app mobile 2" src="~/assets/img/budget-app-mobile-2.png" class="budget-app-phone" />
        <img alt="Budget app desktop" src="~/assets/img/budget-app-desktop.png" class="budget-app-laptop" />
      </div>
      <p class="caption">Every feature of this app was implemented with a mobile-first design. This app is also a Progressive Web App (PWA), which provides a better experience for mobile users.</p>

      <h3>Web App Security</h3>
      <p>I take web app security very seriously. I did a lot of research to find out how to implement auth security correctly to protect my users. There are a lot of ideas out there about how security should be handled, but many of those ideas seem to be "quick and dirty" (i.e. lazy) approaches that do not secure a web app properly. The auth security in this app is implemented by using a refresh token and an access token. The access token has a short expiration period and when it expires the user is given a new access token. This process repeats until the refresh token expires, at which point the user is prompted to login again. The refresh token is also rotated periodically, but it maintains the same expiration time. The ideas that I use for security come mostly from these two posts:</p>
      <ul>
        <li><a href="https://medium.com/hackernoon/the-best-way-to-securely-manage-user-sessions-91f27eeef460" target="_blank">The best way to securely manage user sessions</a></li>
        <li><a href="https://hasura.io/blog/best-practices-of-using-jwt-with-graphql/" target="_blank">The Ultimate Guide to handling JWTs on frontend clients (GraphQL)</a></li>
      </ul>
    </div>

    <div class="content">
      <h2>Content Management System (CMS)</h2>
      <p><a href="https://github.com/SamuelEarl/ink-cms-vue-hapi-neo4j" target="_blank">GitHub Repo</a></p>

      <p>I created this CMS as a hobby project to learn backend development better and to learn Docker. I wrote it as a single-page app with Vue.js in the front-end, hapi.js as the Node.js server, Neo4j as the database, and used I Docker Compose for a multi-container Docker environment.</p>

      <p><strong>These are some of the features in this app:</strong></p>

      <ul>
        <li>Complete authentication flow with user registration, email verification, login, and password reset
        <li>Cookie authentication</li>
        <li>Admin portal where the admin can manage user permissions</li>
        <li>Public facing pages</li>
        <li>Drag and drop to reorder pages</li>
        <li>Show, hide, edit, delete pages</li>
        <li>Data validation on both the server and the client</li>
        <li>Mobile-first design</li>
      </ul>

      <br>

      <div class="cms-images">
        <img alt="CMS pages" src="~/assets/img/cms-pages.png" class="cms-laptop" />
        <img alt="CMS users" src="~/assets/img/cms-users.png" class="cms-laptop" />
      </div>

      <p>Feel free to <a href="https://github.com/SamuelEarl/ink-cms-vue-hapi-neo4j" target="_blank">clone this repo</a> and check out the code. You could follow the instructions in the README to run this app on your computer in Docker, but it might be a bit of a hassle because my environment variables for the database and other features are not included in the repo.</p>

      <p><em><strong>NOTE:</strong> I was experimenting with <code>try/catch/finally</code> blocks in this project, so the API endpoints are constructed a little differently from what you might normally see. I will probably convert this over to serverless functions and then clean up some of the code and features.</em></p>
    </div>

    <div class="content">
      <h2>Interactive Company Org Chart</h2>
      <p>This company org chart is part of a larger project. It uses Vue components and Vuex to handle state management and D3.js to handle the visualizations and chart interactivity.</p>

      <p><strong>These are some of the features in this app:</strong></p>

      <h3>Full Zoom And Pan Capability</h3>
      <img alt="Zoom and pan" src="~/assets/img/zoom-and-pan.gif" class="org-chart-image" />
      <p class="caption">The zoom and pan feature allows users to see and navigate the entire organization easily. This is especially helpful for very large organizations where a list view would be too cumbersome to work with.</p>

      <h3>Search By First Name, Last Name, Or Title</h3>
      <img alt="Search for people" src="~/assets/img/search-for-people.gif" class="org-chart-image" />
      <p class="caption">Users can search for an individual by first name, last name, or title. When the user clicks on one of the people in the search results, that person is centered in the org chart. The user can then perform an action, such as view the person's profile, move the person to another place in the org chart, add a new person to the chart, etc.</p>

      <h3>Click To Center</h3>
      <img alt="Center a person" src="~/assets/img/click-to-center.gif" class="org-chart-image" />
      <p class="caption">When a user clicks on a person's card in the org chart, that person's card will be centered and highlighted for a couple of seconds.</p>

      <p><em><strong>NOTE:</strong> There are still plenty of other features that I need to implement before this will be production ready, but this is a start.</em></p>

    </div>

    <div class="content">
      <h2>Education Website</h2>
      <p>The front-end is a single-page application (SPA) written with Vue.js, Vue Router, and Vuex. Each page is designed to be completely mobile-responsive using the Stylus CSS preprocessor. All UI components (e.g. dropdown menus, accordion menus, modal dialog boxes, image dropzones) are custom made without the use of any pre-built component libraries. The back-end is written in hapi.js (a Node.js framework). The database is Neo4j (a NoSQL graph database).</p>

      <div class="edu-app-images">
        <img alt="iPhone layout" src="~/assets/img/ti-iphone.png" class="edu-app-phone" />
        <img alt="iPhone layout" src="~/assets/img/ti-ipad.png" class="edu-app-tablet" />
        <img alt="iPhone layout" src="~/assets/img/ti-macbook.png" class="edu-app-laptop" />
      </div>

      <p>This website allows users to create accounts, sign-in, create their own courses, and take courses. The website administrator can grant or revoke permissions for various permissions levels. The course pages utilitize WYSIWYG editors with media plugins that allow users to type text or embed images and videos &mdash; similar to content management systems.</p>

      <p><em><strong>NOTE:</strong> This was a project that I worked on a while back as I was learning backend development. I developed it using Docker containers, but it is lacking in some areas (especially the auth flow). I plan on converting the backend to use serverless functions and then I will update the auth flow.</em></p>
    </div>
  </Layout>
</template>

<script>
import Layout from "../../layouts/Layout.vue";

export default {
  components: {
    Layout,
  }
};
</script>

<style lang="stylus" scoped>
@media $xs-up {
  .content {
    margin-bottom: 50px;

    .data-dashboard-image {
      width: 100%;
    }
    // .desktop-image {
    //   max-width: 640px;
    // }

    .budget-app-images {
      display: flex;
      flex-direction: column;
      align-items: center;

      .budget-app-phone {
        width: 175px;
        margin-bottom: 20px;
      }

      .budget-app-laptop {
        width: 100%;
      }
    }

    .cms-images {
      display: flex;
      flex-direction: column;
      align-items: center;

      .cms-laptop {
        width: 100%;
        margin-bottom: 20px;
      }
    }

    .org-chart-image {
      width: 100%;
    }

    .edu-app-images {
      display: flex;
      flex-direction: column;
      align-items: center;

      .edu-app-phone {
        margin-bottom: 20px;
      }

      .edu-app-tablet {
        margin-bottom: 20px;
      }

      .edu-app-laptop {
        max-width: 100%;
        margin-bottom: 20px;
      }
    }

    .caption {
      margin-top: 15px;
      margin-bottom: 30px;
      font-style: italic;
    }
  }
}

@media $m-up {
  .content {

    // .data-dashboard-image {
    //   max-width: 640px;
    // }

    .budget-app-images {
      flex-direction: row;
      justify-content: space-evenly;
      flex-wrap: wrap;

      .budget-app-phone {
        // styles
      }
    }

    .edu-app-images {
      flex-direction: row;
      justify-content: space-evenly;
      flex-wrap: wrap;
    }
  }
}

@media $xl-up {
  .content {

    // .desktop-image {
    //   width: 60%;
    // }

    .budget-app-images {
      align-items: flex-end;
      // justify-content: space-between;
      // flex-wrap: nowrap;
      margin-bottom: 20px;

      .budget-app-phone {
        margin-right: 10px;
        margin-bottom: 0;
      }

      .budget-app-laptop {
        max-width: 60%;
        margin-top: 20px;
      }
    }

    .cms-images {
      // display: flex;
      flex-direction: row;
      // align-items: center;
      justify-content: space-evenly;

      .cms-laptop {
        width: 45%;
        // margin-bottom: 20px;
      }
    }
  }
}
</style>
