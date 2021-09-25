---
title: 多次元スキーマとデータの概要
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6b63a5d75bf4bc5d38e2b3efa3f53da5b221139b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558157"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>多次元スキーマとデータの概要

**適用先:** Access 2013、Office 2013

## <a name="understanding-multidimensional-schemas"></a>多次元スキーマについて

ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される *キューブ* です。

*次元* は、ビジネス エンティティから派生する多次元データベースの独立したデータのカテゴリです。次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。

*階層* は、次元の集計パスです。次元には、複数レベルの粒度があり、そこには親子関係 があります。階層によって、レベル間の関係が定義されます。

*レベル* は、階層内の集計の手順です。複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。

*メンバー* は、次元のデータ アイテムです。一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。

キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。

## <a name="dimensions"></a>Dimensions

キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。

たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。

Geography 次元には、以下の一連のメンバーが含まれます。

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarchies

階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。

## <a name="levels"></a>Levels

上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。

各レベルには、以下のメンバーがあります。

  - The World = {All}


  - 大陸 = {北アメリカ, ヨーロッパ}

  - 国 = {カナダ、米国、英国、ドイツ}

  - Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-Standard Edition, USA-SW, イングランド, アイルランド, スコットランド, ウェールズ, ドイツ-北, ドイツ南}

  - Cities = {Ottawa, Toronto, Vancouver, カルガリー, シアトル, ボイシ, ロサンゼルス, ヒューストン, シュリーブポート, マイアミ, ボストン, ニューヨーク, ロンドン, ドーバー, グラスゴー, エジンバラ, カーディフ, ペンブローク, ベルファスト, ベルリン, ハンブルグ, ミュンヘン, シュトゥットガルト}

## <a name="members"></a>メンバー

階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。

- {All}(親の){ヨーロッパ、北アメリカ}
- {北アメリカ}(親の){カナダ、米国}
- {USA}(親の){USA-NE, USA-NW, USA-Standard Edition, USA-SW}
- {USA-NW}(親の){ボイシ, シアトル}

メンバーは各次元で 1 つ以上の階層に統合できます。

この例では、別の特性も示しています。Year-Week 階層の Week レベルの一部のメンバーは、Year-Quarter 階層の任意のレベルに表示されません。 つまり、階層に次元のすべてのメンバーを含める必要はありません。
