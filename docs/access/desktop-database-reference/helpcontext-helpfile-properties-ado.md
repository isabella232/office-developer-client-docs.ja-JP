---
title: helpcontext プロパティと HelpFile プロパティ (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291993"
---
# <a name="helpcontext-helpfile-properties-ado"></a>helpcontext プロパティと HelpFile プロパティ (ADO)

**適用先:** Access 2013、Office 2013

[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。

## <a name="return-values"></a>戻り値

- **HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。

- **HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 (**String**) の値を返します。

## <a name="remarks"></a>注釈

**HelpFile** プロパティでヘルプ ファイルが指定されている場合、**HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、**HelpContext** プロパティは 0 を返し、**HelpFile** プロパティは長さ 0 の文字列 ("") を返します。

