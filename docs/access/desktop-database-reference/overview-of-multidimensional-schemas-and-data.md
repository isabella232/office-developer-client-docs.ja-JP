---
title: 多次元スキーマとデータの概要
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288155"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>多次元スキーマとデータの概要

**適用先:** Access 2013、Office 2013

## <a name="understanding-multidimensional-schemas"></a>多次元スキーマについて

ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。

*次元*は、ビジネス エンティティから派生する多次元データベースの独立したデータのカテゴリです。次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。

*階層*は、次元の集計パスです。次元には、複数レベルの粒度があり、そこには親子関係 があります。階層によって、レベル間の関係が定義されます。

*レベル*は、階層内の集計の手順です。 複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。

*メンバー*は、次元のデータ アイテムです。 一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。

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


  - 大陸: {北アメリカ、ヨーロッパ}

  - 国 = {カナダ、米国、英国、ドイツ}

  - 地域 = {カナダ-東、カナダ-西、usa-NE、usa-NW、usa-中南米、usa-SW、英国、アイルランド、スコットランド、ウェールズ、ドイツ-北、ドイツ-南}

  - 都市 = {Ottawa, トロント, Vancouver, calgary, シアトル, ボイシ, Los ロサンゼルス, ヒューストン, Shreveport, Miami, ボストン, ニューヨーク,, Dover, Glasgow,, cardiff, Pembroke, ベルギー fast, ベルリン, Hamburg, ミュンヘン, シュトゥットガルト}

## <a name="members"></a>Members

階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。

- いずれ(の親){ヨーロッパ、北アメリカ}
- {北アメリカ}(の親){カナダ、USA}
- 英語(の親){米国-NE、USA-NW、USA-SE、USA-SW}
- {米国-NW}(の親){ボイシ, シアトル}

メンバーは各次元で 1 つ以上の階層に統合できます。

また、この例では、年単位階層の週レベルの一部のメンバーが年四半期の階層のどのレベルにも表示されないということも示しています。 つまり、階層に次元のすべてのメンバーを含める必要はありません。

## <a name="understanding-multidimensional-schemas"></a>多次元スキーマについて

ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。

*次元*は、ビジネス エンティティから派生する多次元データベースの独立したデータのカテゴリです。次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。

*階層*は、次元の集計パスです。次元には、複数レベルの粒度があり、そこには親子関係 があります。階層によって、レベル間の関係が定義されます。

*レベル*は、階層内の集計の手順です。 複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。

*メンバー*は、次元のデータ アイテムです。 一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。

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


- 大陸: {北アメリカ、ヨーロッパ}

- 国 = {カナダ、米国、英国、ドイツ}

- 地域 = {カナダ-東、カナダ-西、usa-NE、usa-NW、usa-中南米、usa-SW、英国、アイルランド、スコットランド、ウェールズ、ドイツ-北、ドイツ-南}

- 都市 = {Ottawa, トロント, Vancouver, calgary, シアトル, ボイシ, Los ロサンゼルス, ヒューストン, Shreveport, Miami, ボストン, ニューヨーク,, Dover, Glasgow,, cardiff, Pembroke, ベルギー fast, ベルリン, Hamburg, ミュンヘン, シュトゥットガルト}

## <a name="members"></a>Members

階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。

- いずれ(の親){ヨーロッパ、北アメリカ}

- {北アメリカ}(の親){カナダ、USA}

- 英語(の親){米国-NE、USA-NW、USA-SE、USA-SW}

- {米国-NW}(の親){ボイシ, シアトル}

メンバーは各次元で 1 つ以上の階層に統合できます。

また、この例では、年単位階層の週レベルの一部のメンバーが年四半期の階層のどのレベルにも表示されないということも示しています。 つまり、階層に次元のすべてのメンバーを含める必要はありません。

