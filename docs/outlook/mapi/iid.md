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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800434"
---
# <a name="iid"></a>IID

  
  
**適用されます**: Outlook 
  
MAPI インターフェイスの識別子を記述するために使用する[GUID](guid.md)構造体について説明します。 
  
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

**GUID**構造体を参照してください。 
  
## <a name="remarks"></a>備考

MAPI インターフェイスを一意に識別して、特定のインターフェイスをオブジェクトに関連付けるには、 **IID**の構造体が使用されます。 などの場合、クライアントへの呼び出し[IMAPISession::OpenEntry](imapisession-openentry.md)フォルダーを開き、クライアント パラメーターを設定_lpInterface_ **IID**を指すように、 [IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを表します。 MAPI では、IID_IMAPIFolder に**IMAPIFolderIID**を定義します。 **IID**の構造は、OLE インターフェイスを一意に識別するのにも使用されます。 
  
MAPI インターフェイスの特定の**IID**の構造体のすべては、Mapiguid.h ヘッダー ファイルで定義されます。 
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)


[MAPI の構造](mapi-structures.md)

