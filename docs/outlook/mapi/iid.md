---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c73dac549ec54d7e2dfd67a1f54031001a77684e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630818"
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

## <a name="members"></a>メンバー

GUID 構造 **を参照** してください。 
  
## <a name="remarks"></a>注釈

**IID 構造は**、MAPI インターフェイスを一意に識別し、特定のインターフェイスをオブジェクトに関連付ける場合に使用します。 たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出してフォルダーを開く場合、クライアントは [、IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを表す **IID** を指す _lpInterface_ パラメーターを設定します。 MAPI では **、IMAPIFolderIID** を使用するIID_IMAPIFolder。 **IID** 構造は、OLE インターフェイスを一意に識別するためにも使用されます。 
  
MAPI インターフェイスの **特定の IID** 構造はすべて、Mapiguid.h ヘッダー ファイルで定義されます。 
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)


[MAPI の構造](mapi-structures.md)

