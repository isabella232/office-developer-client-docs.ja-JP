---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800772"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**適用対象**: Outlook 
  
現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>パラメーター

 _lpUid_
  
> [in]プロファイルのセクションを開くことを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 _LpUid_パラメーターに NULL を渡すことと、呼び出し元のプロファイル セクションが表示されます。 
    
 _ulFlags_
  
> [in]プロファイル セクションを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションでは、呼び出し元に完全にアクセス可能です。 プロファイル セクションがアクセスできない場合は、後続のオブジェクトの呼び出しを行うことができますと、エラーです。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、オブジェクトが読み取り専用で開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
 _lppProfileObj_
  
> [out]開かれているプロファイル セクションへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイル セクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> しようとは、読み取り専用のプロファイル セクションを変更するか、呼び出し元が十分なアクセス許可を持っているオブジェクトへのアクセスにしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_に渡されたエントリの識別子に関連付けられているプロファイルのセクションではありません。
    
MAPI_E_UNKNOWN_FLAGS 
  
> 予約またはサポートされていないフラグを使用し、操作が完了しなかったため、します。
    
## <a name="remarks"></a>注釈

サポートのすべてのオブジェクトの**IMAPISupport::OpenProfileSection**メソッドを実装します。 サービス プロバイダーおよびメッセージ サービスは、プロファイルのセクションを開くし、 **IProfSect**インターフェイスの実装へのポインターを取得する**OpenProfileSection**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 _UlFlags_パラメーターで MAPI_MODIFY フラグを設定して、アクセス許可が十分でない限り、 **OpenProfileSection**は読み取り専用のプロファイル セクションを開きます。 このフラグを設定した場合、読み取り/書き込みアクセス許可は保証されません。付与されたアクセス許可は、現在のアクセス権とオブジェクトによって異なります。 
  
**OpenProfileSection**は、読み取り専用で存在しないプロファイル セクションを開こうとすると、MAPI_E_NOT_FOUND を返します。 場合は**OpenProfileSection**は、読み取り/書き込みとして存在しないプロファイル セクションを開こうとすると、プロファイルのセクションを作成し、 **IProfSect**ポインターを返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

