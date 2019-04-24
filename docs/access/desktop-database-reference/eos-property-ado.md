---
title: EOS プロパティ (ADO Access デスクトップデータベースリファレンス))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293526"
---
# <a name="eos-property-ado"></a><span data-ttu-id="7e72f-102">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e72f-102">EOS property (ADO)</span></span>


<span data-ttu-id="7e72f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e72f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e72f-104">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7e72f-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e72f-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e72f-105">Return values</span></span>

<span data-ttu-id="7e72f-p101">現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="7e72f-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="7e72f-p102">ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e72f-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

