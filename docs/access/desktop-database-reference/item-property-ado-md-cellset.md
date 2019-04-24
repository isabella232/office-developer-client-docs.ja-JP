---
title: Item プロパティ (ADO MD Cellset)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290868"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="3df50-102">Item プロパティ (ADO MD Cellset)</span><span class="sxs-lookup"><span data-stu-id="3df50-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="3df50-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3df50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3df50-104">座標を使用して、セルセットからセルを取得します。</span><span class="sxs-lookup"><span data-stu-id="3df50-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df50-105">構文</span><span class="sxs-lookup"><span data-stu-id="3df50-105">Syntax</span></span>

<span data-ttu-id="3df50-106">*セルのセル* = \*\* セットを設定します。アイテム (*位置*)</span><span class="sxs-lookup"><span data-stu-id="3df50-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="3df50-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3df50-107">Parameters</span></span>

|<span data-ttu-id="3df50-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3df50-108">Parameter</span></span>|<span data-ttu-id="3df50-109">説明</span><span class="sxs-lookup"><span data-stu-id="3df50-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3df50-110">*Positions*</span><span class="sxs-lookup"><span data-stu-id="3df50-110">*Positions*</span></span> |<span data-ttu-id="3df50-111">セルを一意に指定する値の**バリアント型 (Variant** ) の配列です。</span><span class="sxs-lookup"><span data-stu-id="3df50-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="3df50-112">*Positions* は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3df50-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="3df50-113">-位置番号の配列</span><span class="sxs-lookup"><span data-stu-id="3df50-113">- An array of position numbers</span></span><br/><span data-ttu-id="3df50-114">-メンバ名の配列</span><span class="sxs-lookup"><span data-stu-id="3df50-114">- An array of member names</span></span><br/><span data-ttu-id="3df50-115">-序数の位置</span><span class="sxs-lookup"><span data-stu-id="3df50-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="3df50-116">注釈</span><span class="sxs-lookup"><span data-stu-id="3df50-116">Remarks</span></span>

<span data-ttu-id="3df50-p102">**Item** プロパティを使用して、[Cellset](cellset-object-ado-md.md) オブジェクト内の [Cell](cell-object-ado-md.md) オブジェクトを返します。**Item** プロパティによって、引数 *Positions* に対応するセルが見つからない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3df50-p102">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object. If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="3df50-119">**Item** プロパティは **Cellset** オブジェクトの既定プロパティです。</span><span class="sxs-lookup"><span data-stu-id="3df50-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="3df50-120">次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="3df50-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="3df50-p104">引数 *Positions* には、返すセルを指定します。セルは、位置を表す序数または各軸に沿った位置によって指定できます。各軸に沿った位置によってセルを指定する場合は、位置の数値またはメンバーの名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3df50-p104">The *Positions* argument specifies which cell to return. You can specify the cell by ordinal position or by the position along each axis. When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="3df50-p105">位置を表す序数は、**Cellset** 内のセルを一意に識別する数です。概念的には、**Cellset** 内のセルは **Cellset** が *p* 次元の配列であるかのように番号が付けられます。ここで、*p* は軸の数です。セルは行優先でアドレス指定されます。</span><span class="sxs-lookup"><span data-stu-id="3df50-p105">The ordinal position is a number that uniquely identifies one cell within the **Cellset**. Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes. Cells are addressed in row-major order.</span></span>

<span data-ttu-id="3df50-p106">**Item** にメンバー名を文字列として渡す場合、メンバーの軸の数値識別子は昇順で記載する必要があります。軸内では、次元のネストの昇順で記載する必要があります。つまり、最も外側の次元のメンバーを最初に記載し、その後に内側の次元のメンバーを記載します。各次元は個別の文字列で表し、メンバーの文字列の一覧はコンマで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="3df50-p106">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers. Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions. Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="3df50-p107">[!メモ] データ プロバイダーによっては、メンバー名によるセルの取得がサポートされていない場合があります。詳細については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3df50-p107">Retrieving cells by member name may not be supported by your data provider. See the documentation for your provider for more information.</span></span>


