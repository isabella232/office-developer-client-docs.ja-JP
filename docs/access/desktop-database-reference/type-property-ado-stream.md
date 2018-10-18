---
title: Type プロパティ (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602742"
---
# <a name="type-property-ado-stream"></a>Type プロパティ (ADO Stream)


**適用されます**Access 2013 |。Office 2013

[Stream](stream-object-ado.md) (バイナリまたはテキスト) に格納されているデータの種類を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[Stream](streamtypeenum.md) オブジェクトに格納されたデータの種類を示す **StreamTypeEnum** 値を設定または取得します。既定値は **adTypeText** です。ただし、バイナリ データが新しい空の **Stream** に書き込まれる場合、 **Type** は **adTypeBinary** に変更されます。

## <a name="remarks"></a>解説

**Type** プロパティは、現在の位置が **Stream** の先頭 ([Position](position-property-ado.md) が 0) である場合にのみ値の取得および設定が可能であり、その他の位置である場合は値の取得のみ可能です。

**Type** プロパティによって、 **Stream** の読み取りと書き込みに使用するメソッドが決まります。テキスト **Stream** の場合は、 [ReadText](readtext-method-ado.md) および [WriteText](writetext-method-ado.md) を使用します。バイナリ **Stream** の場合は、 [Read](read-method-ado.md) および [Write](write-method-ado.md) を使用します。

