---
title: EOS プロパティ (ADO のデスクトップのデータベース参照のアクセス))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32b76259f9be90ebd60cbc8c618a4d2bb80de165
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870122"
---
# <a name="eos-property-ado"></a><span data-ttu-id="ad013-102">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ad013-102">EOS property (ADO)</span></span>


<span data-ttu-id="ad013-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ad013-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad013-104">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ad013-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad013-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="ad013-105">Return values</span></span>

<span data-ttu-id="ad013-p101">現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="ad013-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="ad013-p102">ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad013-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

