---
title: Unicode 列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804221"
---
# <a name="working-with-unicode-columns"></a>Unicode 列の操作

  
  
**適用対象**: Outlook 
  
PT_STRING8 プロパティの型であり、標準の 8 ビット文字または 16 ビット Unicode 文字は、PT_UNICODE プロパティの型は、使用して、テーブル内の文字列を表すことができます。 テーブルの実装側は、自由に、それぞれのテーブルが Unicode 文字列をサポートするかどうかを選択します。 Unicode では、機能セットを拡張することによって、クライアントとサービス ・ プロバイダーの両方の値を追加、ためには、Unicode をサポート可能な限りことをお勧めします。 
  
テーブルの多くのメソッドは、Unicode を使用する、文字列プロパティの値が期待どおりかどうかを決定するフラグを受け入れます。 入力で MAPI_UNICODE フラグを指定することを示しますテーブル実装する呼び出しで渡されるすべての文字列プロパティの値が Unicode 文字列であり、PT_UNICODE のプロパティの種類があること。 出力では、このフラグは、返される文字列のすべてのプロパティ値に Unicode 文字列では、可能な場合を示します。 フラグが入力または出力の意味を持つかどうかは、このメソッドによって異なります。 Unicode をサポートしていませんし、MAPI_UNICODE フラグが渡されるテーブルの実装では、MAPI_E_BAD_CHAR_WIDTH の値を返します。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

