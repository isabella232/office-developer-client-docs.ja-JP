---
title: lineseparator プロパティ (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289950"
---
# <a name="lineseparator-property-ado"></a>lineseparator プロパティ (ADO)


**適用先:** Access 2013、Office 2013

テキスト [Stream](stream-object-ado.md) オブジェクトの行区切り文字として使用するバイナリ文字を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[Stream](lineseparatorsenum.md) で使う行区切り文字を示す **LineSeparatorsEnum** 値を設定または取得します。 既定値は **adCRLF** です。

## <a name="remarks"></a>注釈

**LineSeparator** は、テキスト **Stream** の内容を読むときに行を解釈するために使います。行は、[SkipLine](skipline-method-ado.md) メソッドで読み飛ばすこともできます。

**LineSeparator** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) だけに使用します。 **Type** が **adTypeBinary** の場合、このプロパティは無視されます。

