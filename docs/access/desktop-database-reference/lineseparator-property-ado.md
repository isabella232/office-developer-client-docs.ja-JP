---
title: LineSeparator プロパティ (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 447acfe8c498975b41ce007f8abd669ade8ee6a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602340"
---
# <a name="lineseparator-property-ado"></a>LineSeparator プロパティ (ADO)


**適用先**: Access 2013、Office 2013

テキスト [Stream](stream-object-ado.md) オブジェクトの行区切り文字として使用するバイナリ文字を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

[Stream](lineseparatorsenum.md) で使う行区切り文字を示す **LineSeparatorsEnum** 値を設定または取得します。既定値は **adCRLF** です。

## <a name="remarks"></a>注釈

**LineSeparator** は、テキスト **Stream** の内容を読むときに行を解釈するために使います。行は、[SkipLine](skipline-method-ado.md) メソッドで読み飛ばすこともできます。

**LineSeparator** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) だけに使用します。**Type** が **adTypeBinary** の場合、このプロパティは無視されます。

