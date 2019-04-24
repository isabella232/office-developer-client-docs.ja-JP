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
# <a name="skipline-method-ado"></a>SkipLine メソッド (ADO)


**適用先:** Access 2013、Office 2013

テキスト ストリームを読み取っているときに、1 行全体をスキップします。

## <a name="syntax"></a>構文

*ストリーム*。SkipLine

## <a name="remarks"></a>注釈

次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。[EOS](eos-property-ado.md) を越えてスキップしようとした場合は、**EOS** が現在の位置になります。

**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。

