---
title: SetEOS メソッド (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f3b1ee81928a8da77cc3edff7f1feffb7196bba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722761"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="95bb2-102">SetEOS メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="95bb2-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="95bb2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="95bb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95bb2-104">ストリームの末尾の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="95bb2-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bb2-105">構文</span><span class="sxs-lookup"><span data-stu-id="95bb2-105">Syntax</span></span>

<span data-ttu-id="95bb2-106">*ストリーム*。SetEOS</span><span class="sxs-lookup"><span data-stu-id="95bb2-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="95bb2-107">解説</span><span class="sxs-lookup"><span data-stu-id="95bb2-107">Remarks</span></span>

<span data-ttu-id="95bb2-p101">**SetEOS** は、現在の [Position](eos-property-ado.md) がストリームの末尾になるように [EOS](position-property-ado.md) プロパティの値を更新します。現在の位置より後ろにあったバイト値や文字はすべて切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="95bb2-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="95bb2-110">[Write](write-method-ado.md)、[WriteText](writetext-method-ado.md)、および [CopyTo](copyto-method-ado.md) の各メソッドでは、既存の **Stream** オブジェクト内の余分な値は切り捨てられないため、これらのバイト値や文字を切り捨てるには、 **SetEOS** でストリームの新しい末尾の位置を設定してください。</span><span class="sxs-lookup"><span data-stu-id="95bb2-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="95bb2-111">**EOS** をストリームの実際の末尾より前の位置に設定すると、新しい **EOS** 位置より後ろのデータはすべて失われます。</span><span class="sxs-lookup"><span data-stu-id="95bb2-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
