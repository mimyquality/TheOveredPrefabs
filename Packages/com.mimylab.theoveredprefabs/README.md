# The Overed Prefabs

VRChatのアバターの負荷検証用に、特定パフォーマンスを悪化させるためだけのプレハブ群です。  

**Packages > The Overed Prefabs > Runtime > Prefabs** に各種パフォーマンスランク組み合わせ用のプレハブが入っています。  
**Packages > The Overed Prefabs > Runtime > Scenes** に各種プレハブを組み合わせた構築済みサンプルアバターが配置されたシーンが入っています。  

> [!IMPORTANT]
> シーンは複製して Assets 以下のフォルダーに移してから編集してください。  
> アバターのプレハブもアップロード後の BPID 保持のため、シーン上に保存するか Prefab Variant にしてから編集してください。  

参考:パフォーマンスランク一覧  
<https://creators.vrchat.com/avatars/avatar-performance-ranking-system/#pc-limits>  

## Avatar

VRCSDK のサンプルアバターから最低限でセットアップしてあるだけのアバターです。  
パフォーマンスランク毎に見分けが付けられるよう派生させた **Avatar_Good**, **Avatar_Medium**, **Avatar_Poor**, **Avatar_VeryPoor**, **Avatar_LegendaryPoor**,  があります。  

- Triangles : 9,012
- Bounds Size : (2.4, 2.4, 2.4)
- Skinned Meshs : 1
- Material Slots : 2
- Animators : 1
- Bones : 130

## SkinnedMesh

SkinnedMesh Renderer 関連のパフォーマンスが悪化するプレハブです。以下の項目の数値が増加します。  

| Prefab 名 | Triangles | Skinned Meshes | Material Slots | Bones |
| --- | --- | --- | --- | --- |
| SkinnedMesh_Medium | 27,552 | 7 | 7 | 35 |
| SkinnedMesh_Poor | 59,040 | 15 | 15 | 75 |
| SkinnedMesh_VeryPoor | 236,160 | 15 | 15 | 75 |
| SkinnedMesh_LegendaryPoor | 944,640 | 15 | 15 | 75 |

## Physbone

Physbone 関連のパフォーマンスが悪化するプレハブです。以下の項目の数値が増加します。  

| Prefab 名 | PB Components | PB Affected Transforms | PB Colliders | PB Collision Check Count |
| --- | --- | --- | --- | --- |
| Physbone_Good | 8 | 64 | 2 | 112 |
| Physbone_Medium | 16 | 128 | 4 | 224 |
| Physbone_Poor | 32 | 256 | 8 | 448 |
| Physbone_VeryPoor | 64 | 512 | 16 | 896 |
| Physbone_LegendaryPoor | 128 | 1,024 | 32 | 1,792 |

## ParticleSystem

ParticleSystem 関連のパフォーマンスが悪化するプレハブです。以下の項目の数値が増加します。  

| Prefab 名 | Particle Systems | Total Max Particles | Total Max Mesh Particle Polys | Particle Trails | Particle Collision | Material Slots |
| --- | --- | --- | --- | --- | --- | --- |
| ParticleSystem_Medium | 8 | 1,000 | 0 | false | true | 8 |
| ParticleSystem_Poor | 16 | 2,496 | 0 | false | true | 16 |
| ParticleSystem_VeryPoor | 16 | 4,800 | 0 | false | true | 16 |
| ParticleSystem_LegendaryPoor | 16 | 9,600 | 0 | false | true | 16 |
