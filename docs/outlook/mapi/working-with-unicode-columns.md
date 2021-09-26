---
title: Unicode 列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 762d8acf3ad006380611025fcfce7675c4a3f0bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629432"
---
# <a name="working-with-unicode-columns"></a>Unicode 列の操作

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の文字列は、プロパティ型 PT_STRING8 または 16 ビット Unicode 文字 (プロパティ型 PT_UNICODE) である標準の 8 ビット文字を使用して表されます。 テーブル実装者は、テーブルが Unicode 文字列をサポートするかどうかを自由に選択できます。 Unicode は機能セットを拡張してクライアントとサービス プロバイダーの両方に値を追加しますので、可能な限り Unicode をサポートする方法をお勧めします。 
  
多くのテーブル メソッドは、文字列プロパティの値が Unicode と予想されるかどうかを示すフラグを受け入れています。 入力時に、MAPI_UNICODE フラグを指定すると、呼び出しで渡される文字列プロパティの値はすべて Unicode 文字列であり、プロパティの種類は PT_UNICODE です。 出力時に、このフラグは、返される文字列プロパティの値はすべて、可能であれば Unicode 文字列である必要があります。 フラグが入力または出力の意味を持つかどうかは、メソッドによって異なります。 Unicode をサポートしていないテーブル実装者は、MAPI_UNICODE値をMAPI_E_BAD_CHAR_WIDTHします。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

