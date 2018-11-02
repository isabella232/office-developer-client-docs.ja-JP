---
title: SkipLine メソッド (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923925"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="241c1-102">SkipLine メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="241c1-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="241c1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="241c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="241c1-104">テキスト ストリームを読み取っているときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="241c1-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="241c1-105">構文</span><span class="sxs-lookup"><span data-stu-id="241c1-105">Syntax</span></span>

<span data-ttu-id="241c1-106">*ストリーム*。SkipLine</span><span class="sxs-lookup"><span data-stu-id="241c1-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="241c1-107">解説</span><span class="sxs-lookup"><span data-stu-id="241c1-107">Remarks</span></span>

<span data-ttu-id="241c1-p101">次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。 [EOS](eos-property-ado.md) を越えてスキップしようとした場合は、 **EOS** が現在の位置になります。</span><span class="sxs-lookup"><span data-stu-id="241c1-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="241c1-111">**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。</span><span class="sxs-lookup"><span data-stu-id="241c1-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

