---
title: EOS プロパティ (ADO のデスクトップのデータベース参照のアクセス))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477821"
---
# <a name="eos-property-ado"></a><span data-ttu-id="5f484-102">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f484-102">EOS Property (ADO)</span></span>


<span data-ttu-id="5f484-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f484-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5f484-104">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5f484-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f484-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f484-105">Return Values</span></span>

<span data-ttu-id="5f484-p101">現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="5f484-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="5f484-p102">ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5f484-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

