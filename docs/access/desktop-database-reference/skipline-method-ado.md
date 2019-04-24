---
title: SkipLine メソッド (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314561"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="b5f4c-102">SkipLine メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="b5f4c-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="b5f4c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5f4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5f4c-104">テキスト ストリームを読み取っているときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="b5f4c-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f4c-105">構文</span><span class="sxs-lookup"><span data-stu-id="b5f4c-105">Syntax</span></span>

<span data-ttu-id="b5f4c-106">*ストリーム*。SkipLine</span><span class="sxs-lookup"><span data-stu-id="b5f4c-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f4c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b5f4c-107">Remarks</span></span>

<span data-ttu-id="b5f4c-p101">次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。[EOS](eos-property-ado.md) を越えてスキップしようとした場合は、**EOS** が現在の位置になります。</span><span class="sxs-lookup"><span data-stu-id="b5f4c-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="b5f4c-111">**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。</span><span class="sxs-lookup"><span data-stu-id="b5f4c-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

