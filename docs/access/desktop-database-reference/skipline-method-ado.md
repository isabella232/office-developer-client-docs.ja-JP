---
title: SkipLine メソッド (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17279e2d36e101b2232a7a9bc0519ad6d25ee0b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589114"
---
# <a name="skipline-method-ado"></a>SkipLine メソッド (ADO)


**適用先**: Access 2013、Office 2013

テキスト ストリームを読み取っているときに、1 行全体をスキップします。

## <a name="syntax"></a>構文

*Stream*.SkipLine

## <a name="remarks"></a>注釈

次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。[EOS](eos-property-ado.md) を越えてスキップしようとした場合は、**EOS** が現在の位置になります。

**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。

