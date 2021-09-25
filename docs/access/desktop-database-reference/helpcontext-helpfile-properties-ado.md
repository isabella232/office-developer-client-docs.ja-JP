---
title: HelpContext、 HelpFile プロパティ (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 860d300d0be62e2db17776c03289b0ef8a3d4029
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615432"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext、 HelpFile プロパティ (ADO)

**適用先**: Access 2013、Office 2013

[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。

## <a name="return-values"></a>戻り値

- **HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。

- **HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 (**String**) の値を返します。

## <a name="remarks"></a>注釈

**HelpFile** プロパティでヘルプ ファイルが指定されている場合、**HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、**HelpContext** プロパティは 0 を返し、**HelpFile** プロパティは長さ 0 の文字列 ("") を返します。

