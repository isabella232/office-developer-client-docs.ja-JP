---
title: EOS プロパティ (ADO のデスクトップのデータベース参照のアクセス))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716601"
---
# <a name="eos-property-ado"></a><span data-ttu-id="6d283-102">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="6d283-102">EOS property (ADO)</span></span>


<span data-ttu-id="6d283-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6d283-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d283-104">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d283-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d283-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="6d283-105">Return values</span></span>

<span data-ttu-id="6d283-p101">現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="6d283-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="6d283-p102">ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6d283-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

