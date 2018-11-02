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
# <a name="skipline-method-ado"></a>SkipLine メソッド (ADO)


**適用されます**Access 2013、Office 2013。

テキスト ストリームを読み取っているときに、1 行全体をスキップします。

## <a name="syntax"></a>構文

*ストリーム*。SkipLine

## <a name="remarks"></a>解説

次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。 [EOS](eos-property-ado.md) を越えてスキップしようとした場合は、 **EOS** が現在の位置になります。

**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。

