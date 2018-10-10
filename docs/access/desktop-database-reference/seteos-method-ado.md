---
title: SetEOS メソッド (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 456bbf7c7235d0db01b29372ee8f70c364263cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476196"
---
# <a name="seteos-method-ado"></a>SetEOS メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

ストリームの末尾の位置を設定します。

## <a name="syntax"></a>構文

*ストリーム*。SetEOS

## <a name="remarks"></a>解説

**SetEOS** は、現在の [Position](eos-property-ado.md) がストリームの末尾になるように [EOS](position-property-ado.md) プロパティの値を更新します。現在の位置より後ろにあったバイト値や文字はすべて切り捨てられます。

[Write](write-method-ado.md)、[WriteText](writetext-method-ado.md)、および [CopyTo](copyto-method-ado.md) の各メソッドでは、既存の **Stream** オブジェクト内の余分な値は切り捨てられないため、これらのバイト値や文字を切り捨てるには、 **SetEOS** でストリームの新しい末尾の位置を設定してください。


> [!WARNING]
> <P><STRONG>EOS</STRONG> をストリームの実際の末尾より前の位置に設定すると、新しい <STRONG>EOS</STRONG> 位置より後ろのデータはすべて失われます。</P>


