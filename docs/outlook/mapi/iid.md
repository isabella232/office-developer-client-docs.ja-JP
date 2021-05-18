---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411597"
---
# <a name="iid"></a>IID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI インターフェイスの [識別子](guid.md) を記述するために使用される GUID 構造について説明します。 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

GUID 構造 **を参照** してください。 
  
## <a name="remarks"></a>注釈

**IID 構造は**、MAPI インターフェイスを一意に識別し、特定のインターフェイスをオブジェクトに関連付ける場合に使用します。 たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出してフォルダーを開く場合、クライアントは [、IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを表す **IID** を指す _lpInterface_ パラメーターを設定します。 MAPI では **、IMAPIFolderIID** を使用するIID_IMAPIFolder。 **IID** 構造は、OLE インターフェイスを一意に識別するためにも使用されます。 
  
MAPI インターフェイスの **特定の IID** 構造はすべて、Mapiguid.h ヘッダー ファイルで定義されます。 
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)


[MAPI の構造](mapi-structures.md)

