---
title: Unicode 列の使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325572"
---
# <a name="working-with-unicode-columns"></a>Unicode 列の使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の文字列は、プロパティの種類が PT_STRING8 の標準の8ビット文字、またはプロパティの種類が PT_UNICODE である16ビットの Unicode 文字を使用して表すことができます。 表の実装者は、テーブルが Unicode 文字列をサポートしているかどうかを自由に選択できます。 unicode は、機能セットを拡張することによって、クライアントとサービスプロバイダーの両方の値を追加するため、可能な限り unicode をサポートすることをお勧めします。 
  
多くの table メソッドは、文字列プロパティの値が Unicode であることを想定しているかどうかを指定するフラグを受け入れます。 入力時に、MAPI_UNICODE フラグを指定すると、呼び出しに渡されたすべての文字列プロパティの値が UNICODE 文字列であり、プロパティの種類が PT_UNICODE であることをテーブルの実装に示します。 出力時、このフラグは、返されるすべての文字列プロパティ値が Unicode 文字列であることを示します (可能な場合)。 フラグが入力または出力に対して意味を持つかどうかは、メソッドによって決まります。 Unicode をサポートしておらず、MAPI_UNICODE フラグが渡されるテーブル実装では、MAPI_E_BAD_CHAR_WIDTH 値を返します。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

