---
title: State プロパティ (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33933fb71ee3d7541640469eebc650c0f52a9784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922014"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="a875c-102">State プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a875c-102">State property (ADO MD)</span></span>


<span data-ttu-id="a875c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a875c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a875c-104">セルセットの現在の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="a875c-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="a875c-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="a875c-105">Return values</span></span>

<span data-ttu-id="a875c-p101">**Cellset** オブジェクトの現在の状態を示す長整数型 ( [Long](cellset-object-ado-md.md) ) の値を取得します。値の取得のみが可能です。有効な値は、 **adStateClosed** (0) および **adStateOpen** (1) です。</span><span class="sxs-lookup"><span data-stu-id="a875c-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="a875c-108">解説</span><span class="sxs-lookup"><span data-stu-id="a875c-108">Remarks</span></span>

<span data-ttu-id="a875c-p102">[ObjectStateEnum](objectstateenum.md) 定数の名前を使用するには、プロジェクトで ADO タイプ ライブラリが参照されている必要があります。詳細については、「 [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a875c-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

