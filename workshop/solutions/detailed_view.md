# Ajustement de la présentation des résultats

```html
<ul>
  <li style="list-style: none;" ng-repeat="record in vm.invenioSearchResults.hits.hits track by $index">
        <h4><a target="_self" ng-href="/records/{{record.id}}">{{record.metadata.album}}</a></h4>
    <h5 ng-show="record.metadata.artist">{{record.metadata.artist}}</h5>
    <ul>
      <div ng-repeat="author in record.metadata.performers track by $index">
        <li>{{ author }}</li>
      </div>
    </ul>
    <hr />
  </li>
</ul>
```