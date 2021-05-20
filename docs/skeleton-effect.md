#skeleton-effect

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Skeleton Text</title>
  <script type="module" src="https://zababurinsv.github.io/distrib/ionic.esm.js"></script>
  <script nomodule src="https://zababurinsv.github.io/distrib/ionic.js"></script>
  <link rel="stylesheet" href="https://zababurinsv.github.io/distrib/ionic.bundle.css"/>
  <style>
    #data {
  display: none;
}

/* Custom Skeleton Line Height and Margin */
.custom-skeleton ion-skeleton-text {
  line-height: 13px;
}

.custom-skeleton ion-skeleton-text:last-child {
  margin-bottom: 5px;
}
  </style>
</head>

<body>
  <ion-app>
    <ion-header translucent>
      <ion-toolbar>
        <ion-title>Skeleton Text</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <!-- Data to display after skeleton screen -->
<div id="data">
    <div class="ion-padding">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ac eros est. Cras iaculis pulvinar arcu non vehicula. Fusce at quam a eros malesuada condimentum. Aliquam tincidunt tincidunt vehicula.
    </div>
  
    <ion-list>
      <ion-list-header>
        <ion-label>
          Data
        </ion-label>
      </ion-list-header>
      <ion-item>
        <ion-avatar slot="start">
          <img src="./avatar.svg">
        </ion-avatar>
        <ion-label>
          <h3>
            Normal text
          </h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur
          </p>
          <p>
            adipiscing elit.
          </p>
        </ion-label>
      </ion-item>
      <ion-item>
        <ion-thumbnail slot="start">
          <img src="./thumbnail.svg">
        </ion-thumbnail>
        <ion-label>
          <h3>
            Normal text
          </h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur
          </p>
          <p>
            adipiscing elit.
          </p>
        </ion-label>
      </ion-item>
      <ion-item>
        <ion-icon name="call" slot="start"></ion-icon>
        <ion-label>
          <h3>
            Normal text
          </h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur
          </p>
          <p>
            adipiscing elit.
          </p>
        </ion-label>
      </ion-item>
    </ion-list>
  </div>
  
  <!-- Skeleton screen -->
  <div id="skeleton">
    <div class="ion-padding custom-skeleton">
      <ion-skeleton-text animated style="width: 60%"></ion-skeleton-text>
      <ion-skeleton-text animated></ion-skeleton-text>
      <ion-skeleton-text animated style="width: 88%"></ion-skeleton-text>
      <ion-skeleton-text animated style="width: 70%"></ion-skeleton-text>
      <ion-skeleton-text animated style="width: 60%"></ion-skeleton-text>
    </div>
  
    <ion-list>
      <ion-list-header>
        <ion-label>
          <ion-skeleton-text animated style="width: 20%"></ion-skeleton-text>
        </ion-label>
      </ion-list-header>
      <ion-item>
        <ion-avatar slot="start">
          <ion-skeleton-text animated></ion-skeleton-text>
        </ion-avatar>
        <ion-label>
          <h3>
            <ion-skeleton-text animated style="width: 50%"></ion-skeleton-text>
          </h3>
          <p>
            <ion-skeleton-text animated style="width: 80%"></ion-skeleton-text>
          </p>
          <p>
            <ion-skeleton-text animated style="width: 60%"></ion-skeleton-text>
          </p>
        </ion-label>
      </ion-item>
      <ion-item>
        <ion-thumbnail slot="start">
          <ion-skeleton-text animated></ion-skeleton-text>
        </ion-thumbnail>
        <ion-label>
          <h3>
            <ion-skeleton-text animated style="width: 50%"></ion-skeleton-text>
          </h3>
          <p>
            <ion-skeleton-text animated style="width: 80%"></ion-skeleton-text>
          </p>
          <p>
            <ion-skeleton-text animated style="width: 60%"></ion-skeleton-text>
          </p>
        </ion-label>
      </ion-item>
      <ion-item>
        <ion-skeleton-text animated style="width: 27px; height: 27px" slot="start"></ion-skeleton-text>
        <ion-label>
          <h3>
            <ion-skeleton-text animated style="width: 50%"></ion-skeleton-text>
          </h3>
          <p>
            <ion-skeleton-text animated style="width: 80%"></ion-skeleton-text>
          </p>
          <p>
            <ion-skeleton-text animated style="width: 60%"></ion-skeleton-text>
          </p>
        </ion-label>
      </ion-item>
    </ion-list>
  </div>
    </ion-content>
  </ion-app>
  <script>
      function onLoad() {
  const skeletonEl = document.getElementById('skeleton');
  const dataEl = document.getElementById('data');

  setTimeout(() => {
    skeletonEl.style.display = 'none';
    dataEl.style.display = 'block';
  }, 5000);
}
  </script>
</body>

</html>

```