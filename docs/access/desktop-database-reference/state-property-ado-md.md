---
title: State プロパティ (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a389ad273c2d47405ff6dcec6f5b5c42fa0662b8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602441"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="81970-102">State プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="81970-102">State Property (ADO MD)</span></span>


<span data-ttu-id="81970-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="81970-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81970-104">セルセットの現在の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="81970-104">Indicates the current state of the cellset.</span></span>

<span data-ttu-id="81970-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="81970-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="81970-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="81970-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="81970-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="81970-107">Return values</span></span>
>>>>>>> <span data-ttu-id="81970-108">master</span><span class="sxs-lookup"><span data-stu-id="81970-108">master</span></span>

<span data-ttu-id="81970-p101">**Cellset** オブジェクトの現在の状態を示す長整数型 ( [Long](cellset-object-ado-md.md) ) の値を取得します。値の取得のみが可能です。有効な値は、 **adStateClosed** (0) および **adStateOpen** (1) です。</span><span class="sxs-lookup"><span data-stu-id="81970-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="81970-111">解説</span><span class="sxs-lookup"><span data-stu-id="81970-111">Remarks</span></span>

<span data-ttu-id="81970-p102">[ObjectStateEnum](objectstateenum.md) 定数の名前を使用するには、プロジェクトで ADO タイプ ライブラリが参照されている必要があります。詳細については、「 [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81970-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

