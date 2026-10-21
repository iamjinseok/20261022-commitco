# 지도와 3D 모델

코드 블록의 언어를 `geojson`, `stl`로 쓰면 지도와 3D 모델이 됩니다.

## 지도 (geojson)

좌표는 `[경도, 위도]` 순서입니다.

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": { "name": "서울시청" },
      "geometry": { "type": "Point", "coordinates": [126.9779, 37.5665] }
    },
    {
      "type": "Feature",
      "properties": { "name": "서울역에서 시청까지" },
      "geometry": {
        "type": "LineString",
        "coordinates": [[126.9724, 37.5547], [126.9779, 37.5665]]
      }
    }
  ]
}
```

## 3D 모델 (stl)

렌더링되면 마우스로 돌려볼 수 있습니다.

```stl
solid pyramid
  facet normal 0 0 -1
    outer loop
      vertex 0 0 0
      vertex 0 2 0
      vertex 2 2 0
    endloop
  endfacet
  facet normal 0 0 -1
    outer loop
      vertex 0 0 0
      vertex 2 2 0
      vertex 2 0 0
    endloop
  endfacet
  facet normal 0 -0.894 0.447
    outer loop
      vertex 0 0 0
      vertex 2 0 0
      vertex 1 1 2
    endloop
  endfacet
  facet normal 0.894 0 0.447
    outer loop
      vertex 2 0 0
      vertex 2 2 0
      vertex 1 1 2
    endloop
  endfacet
  facet normal 0 0.894 0.447
    outer loop
      vertex 2 2 0
      vertex 0 2 0
      vertex 1 1 2
    endloop
  endfacet
  facet normal -0.894 0 0.447
    outer loop
      vertex 0 2 0
      vertex 0 0 0
      vertex 1 1 2
    endloop
  endfacet
endsolid
```
