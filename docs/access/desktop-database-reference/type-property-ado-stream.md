---
title: Type プロパティ (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306252"
---
# <a name="type-property-ado-stream"></a>Type プロパティ (ADO Stream)


**適用先:** Access 2013、Office 2013

[Stream](stream-object-ado.md) (バイナリまたはテキスト) に格納されているデータの種類を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[Stream](streamtypeenum.md) オブジェクトに格納されたデータの種類を示す **StreamTypeEnum** 値を設定または取得します。既定値は **adTypeText** です。ただし、バイナリ データが新しい空の **Stream** に書き込まれる場合、 **Type** は **adTypeBinary** に変更されます。

## <a name="remarks"></a>注釈

**Type** プロパティは、現在の位置が **Stream** の先頭 ([Position](position-property-ado.md) が 0) である場合にのみ値の取得および設定が可能であり、その他の位置である場合は値の取得のみ可能です。

**Type** プロパティによって、**Stream** の読み取りと書き込みに使用するメソッドが決まります。テキスト **Stream** の場合は、[ReadText](readtext-method-ado.md) および [WriteText](writetext-method-ado.md) を使用します。バイナリ **Stream** の場合は、[Read](read-method-ado.md) および [Write](write-method-ado.md) を使用します。

