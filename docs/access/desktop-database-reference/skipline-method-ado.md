---
title: SkipLine メソッド (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28cb222a3ed0e5497e03efbb7394081c96b4d4ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477932"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="b60ce-102">SkipLine メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="b60ce-102">SkipLine Method (ADO)</span></span>


<span data-ttu-id="b60ce-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b60ce-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b60ce-104">テキスト ストリームを読み取っているときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="b60ce-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b60ce-105">構文</span><span class="sxs-lookup"><span data-stu-id="b60ce-105">Syntax</span></span>

<span data-ttu-id="b60ce-106">*ストリーム*。SkipLine</span><span class="sxs-lookup"><span data-stu-id="b60ce-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="b60ce-107">解説</span><span class="sxs-lookup"><span data-stu-id="b60ce-107">Remarks</span></span>

<span data-ttu-id="b60ce-p101">次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。 [EOS](eos-property-ado.md) を越えてスキップしようとした場合は、 **EOS** が現在の位置になります。</span><span class="sxs-lookup"><span data-stu-id="b60ce-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="b60ce-111">**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。</span><span class="sxs-lookup"><span data-stu-id="b60ce-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

