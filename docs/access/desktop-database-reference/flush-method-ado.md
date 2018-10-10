---
title: メソッドをフラッシュするには、ActiveX データ オブジェクト (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c2d7543d2e9a1229661e572e95b783621aa43fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479112"
---
# <a name="flush-method-ado"></a><span data-ttu-id="28cf0-102">Flush メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="28cf0-102">Flush Method (ADO)</span></span>


<span data-ttu-id="28cf0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="28cf0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="28cf0-104">ADO バッファーに残っている [Stream](stream-object-ado.md) の内容を、 **Stream** に関連付けられた、基になるオブジェクトに反映します。</span><span class="sxs-lookup"><span data-stu-id="28cf0-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="28cf0-105">構文</span><span class="sxs-lookup"><span data-stu-id="28cf0-105">Syntax</span></span>

<span data-ttu-id="28cf0-106">*ストリーム*。フラッシュ</span><span class="sxs-lookup"><span data-stu-id="28cf0-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="28cf0-107">解説</span><span class="sxs-lookup"><span data-stu-id="28cf0-107">Remarks</span></span>

<span data-ttu-id="28cf0-p101">このメソッドを使用すると、基になるオブジェクト (たとえば、 **Stream** オブジェクトのソースの URL で表されるノードやファイル) に、ストリーム バッファーの内容を送ることができます。 **Stream** の内容に加えたすべての変更が確実に書き込まれるようにするには、このメソッドを呼び出す必要があります。ただし、ADO ではバックグラウンドで可能な限り継続してバッファーのフラッシュが行われるので、通常は **Flush** を呼び出す必要はありません。 **Stream** の内容の更新は自動的に行われ、 **Flush** を呼び出すまでキャッシュされるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="28cf0-p101">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object). This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written. However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background. Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="28cf0-112">**Close** メソッドで [Stream](close-method-ado.md) を閉じると、 **Stream** の内容が自動的にフラッシュされるので、 **Close** の直前に明示的に **Flush** を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="28cf0-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>
