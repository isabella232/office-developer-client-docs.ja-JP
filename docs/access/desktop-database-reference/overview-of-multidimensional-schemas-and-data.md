---
title: 多次元スキーマおよびデータの概要
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67bdcdbaa525039f544a7d45cb4411faeee297e8
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937030"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>多次元スキーマおよびデータの概要


**適用されます**Access 2013、Office 2013。

## <a name="understanding-multidimensional-schemas"></a>多次元スキーマについて

ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。

*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。 次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。

*階層*は、ディメンションの集計パスです。 次元には、複数レベルの粒度があり、そこには親子関係 があります。 階層によって、レベル間の関係が定義されます。

*レベル*は、階層内の集計の手順です。 複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。

*メンバー*は、ディメンション内のデータ アイテムです。 一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。

キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。

## <a name="dimensions"></a>次元

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

## <a name="hierarchies"></a>階層

階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。

## <a name="levels"></a>レベル

上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。

各レベルには、以下のメンバーがあります。

  - The World = {All}


  - Continents = {North America, Europe}


  - Countries = {Canada, USA, UK, Germany}


  - Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


  - Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>メンバー

階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。

- {すべて}(親の){ヨーロッパ、北アメリカ。
- {(北アメリカ)。(親の){カナダ、アメリカ合衆国}
- {アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}
- {アメリカ合衆国の NW}(親の){ボイシ、シアトル。

メンバーは各次元で 1 つ以上の階層に統合できます。

この例では、別の特性も示しています。 年週階層の週レベルの一部のメンバーは、4 分の 1 年の階層のどのレベルには表示されません。 つまり、階層に次元のすべてのメンバーを含める必要はありません。

## <a name="understanding-multidimensional-schemas"></a>多次元スキーマについて

ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。

*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。 次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。

*階層*は、ディメンションの集計パスです。 次元には、複数レベルの粒度があり、そこには親子関係 があります。 階層によって、レベル間の関係が定義されます。

*レベル*は、階層内の集計の手順です。 複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。

*メンバー*は、ディメンション内のデータ アイテムです。 一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。

キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。

## <a name="dimensions"></a>次元

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

## <a name="hierarchies"></a>階層

階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。

## <a name="levels"></a>レベル

上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。

各レベルには、以下のメンバーがあります。

- The World = {All}


- Continents = {North America, Europe}


- Countries = {Canada, USA, UK, Germany}


- Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


- Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>メンバー

階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。

- {すべて}(親の){ヨーロッパ、北アメリカ。

- {(北アメリカ)。(親の){カナダ、アメリカ合衆国}

- {アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}

- {アメリカ合衆国の NW}(親の){ボイシ、シアトル。

メンバーは各次元で 1 つ以上の階層に統合できます。

この例では、別の特性も示しています。 年週階層の週レベルの一部のメンバーは、4 分の 1 年の階層のどのレベルには表示されません。 つまり、階層に次元のすべてのメンバーを含める必要はありません。

