---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595203"
---
# <a name="tchar"></a>TCHAR

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ANSI、DBCS、または Unicode の文字列を記述するために使用する Win32 文字の文字列です。 ANSI と DBCS のプラットフォームの TCHAR は次のように定義されます。
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>注釈

Unicode プラットフォームの場合は、TCHAR は WCHAR 型と同じ意味として定義されます。 
  
MAPI クライアントでは、WCHAR または char 型の文字列を表すため、TCHAR データ型を使用できます。 シンボリック定数の UNICODE を定義し、必要な場合に、プラットフォームを制限することを確認します。 MAPI はプラットフォームの情報を解釈し、内部的に TCHAR を適切な文字列に変換します。 MAPI プロパティの型、PT_TSTRING は、TCHAR データ型と同じように動作します。 プラットフォームでは、Unicode をサポートする PT_TSTRING の種類のプロパティはコンパイル時に PT_UNICODE の種類に割り当てられます。 プラットフォームでは、Unicode をサポートしていない、これらのプロパティに PT_STRING8 の種類が割り当てられます。
  
この機能の詳細については、[文字セット](mapi-character-sets.md)と[プロパティの種類の一覧](property-types.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI データ型](mapi-data-types.md)

