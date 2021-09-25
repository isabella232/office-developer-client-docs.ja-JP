---
title: SetEOS メソッド (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0856381b288d38c9fc85b5588857477a9c5fa901
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626079"
---
# <a name="seteos-method-ado"></a>SetEOS メソッド (ADO)

**適用先**: Access 2013、Office 2013

ストリームの末尾の位置を設定します。

## <a name="syntax"></a>構文

*Stream*.SetEOS

## <a name="remarks"></a>注釈

**SetEOS** は、現在の [Position](eos-property-ado.md) がストリームの末尾になるように [EOS](position-property-ado.md) プロパティの値を更新します。現在の位置より後ろにあったバイト値や文字はすべて切り捨てられます。

[Write](write-method-ado.md)、[WriteText](writetext-method-ado.md)、および [CopyTo](copyto-method-ado.md) の各メソッドでは、既存の **Stream** オブジェクト内の余分な値は切り捨てられないため、これらのバイト値や文字を切り捨てるには、 **SetEOS** でストリームの新しい末尾の位置を設定してください。

> [!WARNING]
> **EOS** をストリームの実際の末尾より前の位置に設定すると、新しい **EOS** 位置より後ろのデータはすべて失われます。
