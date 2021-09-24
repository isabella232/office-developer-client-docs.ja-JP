---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: '最終更新日: 2011 年 7 月 23 日'
ms.localizationpriority: high
ms.openlocfilehash: 86eef598a84ed7cd11d1fdcc6350375c6421a029
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549876"
---
# <a name="tchar"></a>TCHAR

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ANSI、DBCS、または Unicode 文字列の記述に使用できる Win32 文字の文字列。 ANSI および DBCS プラットフォームの場合、TCHAR は次のように定義されています。
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>解説

Unicode プラットフォームの場合、TCHAR は WCHAR 型と同義語として定義されています。 
  
MAPI のクライアントでは、TCHAR データ型を使用して WCHAR または char 型のいずれかの文字列を表すことができます。 シンボリック定数 UNICODE を定義し、必要に応じてプラットフォームを制限してください。 MAPI はプラットフォーム情報を解釈し、内部的に TCHAR を適切な文字列に変換します。 MAPI のプロパティ型 (PT_TSTRING) は、TCHAR データ型と同様に機能します。 プラットフォームが Unicode をサポートしている場合は、コンパイル時に PT_UNICODE 型が PT_TSTRING 型のプロパティに割り当てられます。 プラットフォームが Unicode をサポートしていない場合は、これらのプロパティに PT_STRING8 型が割り当てられます。
  
この機能の詳細については、「[文字セット](mapi-character-sets.md)」および「[プロパティの型のリスト](property-types.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI のデータ型](mapi-data-types.md)

