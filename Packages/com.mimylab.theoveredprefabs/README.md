# The Overed Prefabs

VRChatのアバターの負荷検証用に、特定パフォーマンスを悪化させるためだけのプレハブ群です。  
**Packages > The Overed Prefabs > Runtime Prefabs** に各種パフォーマンスランク組み合わせ用のプレハブが入っています。  

参考:パフォーマンスランク一覧
<https://creators.vrchat.com/avatars/avatar-performance-ranking-system/#pc-limits>

## Base_Good

VRCSDK のサンプルアバターから最低限でセットアップしてあるだけのアバターです。  

- Triangles : 9012
- Bounds Size : (2.4, 2.4, 2.4)
- Skinned Meshs : 1
- Material Slots : 2
- Animators : 1
- Bones : 130

## Physbone

Physbone 関連のパフォーマンスが悪化するプレハブです。以下の項目の数値が増加します。  

| Prefab 名 | PB Components | PB Affected Transforms | PB Colliders | PB Collision Check Count |
| --- | --- | --- | --- | --- |
| Physbone_Good | 8 | 64 | 2 | 112 |
| Physbone_Medium | 16 | 128 | 4 | 224 |
| Physbone_Poor | 32 | 256 | 8 | 448 |
| Physbone_VeryPoor | 64 | 512 | 16 | 896 |
| Physbone_LegendaryPoor | 128 | 1024 | 32 | 1792 |

## ParticleSystem

ParticleSystem 関連のパフォーマンスが悪化するプレハブです。以下の項目の数値が増加します。  

| Prefab 名 | Particle Systems | Total Max Particles | Total Max Mesh Particle Polys | Particle Trails | Particle Collision | Material Slots |
| --- | --- | --- | --- | --- | --- | --- |
| ParticleSystem_Medium | 8 | 1000 | 0 | false | true | 8 |
| ParticleSystem_Poor | 16 | 2496 | 0 | false | true | 16 |
| ParticleSystem_VeryPoor | 16 | 4800 | 0 | false | true | 16 |
| ParticleSystem_LegendaryPoor | 16 | 9600 | 0 | false | true | 16 |
