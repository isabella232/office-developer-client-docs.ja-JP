---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800763"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**適用されます**: Outlook 
  
一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造体を作成します。 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameters

 _lpMuid_
  
> 新しい**MAPIUID**構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しい**MAPIUID**構造体が作成されました。 
    
## <a name="remarks"></a>備考

サポートのすべてのオブジェクトの**IMAPISupport::NewUID**メソッドを実装します。 サービス プロバイダーおよびメッセージ サービスは、長期的な一意の識別子を生成する必要があるたびに**NewUID**を呼び出します。 メッセージは、たとえば、プロバイダーを格納、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティに新しく作成したメッセージを配置するには**MAPIUID**を取得する**NewUID**を呼び出すことがあります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**NewUID**メソッドを作成する**MAPIUID**構造体でのログオン時に登録する**MAPIUID**構造体を混同しないでください。 メッセージが MAPI プロバイダーを格納し、別のプロバイダーを作成するエントリの識別子を区別するために使用または[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出すときに登録する**MAPIUID**構造体は、アドレス帳を表します。 この**MAPIUID**の構造体は、ハード コーディングされ、 **NewUID**を呼び出すことによって取得されませんする必要があります。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

