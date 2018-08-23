---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573013"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在のプロファイルからプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]プロファイルのセクションを開くことの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 クライアントは、 _lpUID_パラメーターに NULL を渡す必要がありますされません。 サービス プロバイダーは、メッセージ サービスのエントリ ポイント関数を呼び出すときに、 **MAPIUID**を取得するために NULL を渡すことができます。 
    
 _lpInterface_
  
> [in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 プロファイル セクションの標準的なインタ フェースで (**IProfSect**) が返される NULL を渡すことが発生します。 
    
 _ulFlags_
  
> [in]プロファイル セクションを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了が、[プロファイル] セクションは、呼び出し元に完全に利用可能な前に**OpenProfileSection**を有効にします。 プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生します。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用の権限を持つオブジェクトが開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 クライアントは、プロファイルのプロバイダー セクションへの読み取り/書き込み権限を許可されていません。
    
MAPI_FORCE_ACCESS
  
> 個々 のサービス ・ プロバイダーが所有するものであっても、すべてのプロファイル セクションへのアクセスを許可します。
    
 _lppProfSect_
  
> [out]プロファイル セクションへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイル セクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> しようとは、読み取り専用のプロファイル セクションを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。
    
MAPI_E_NOT_FOUND 
  
> 要求したプロファイル セクションが存在しません。
    
## <a name="remarks"></a>注釈

**IProviderAdmin::OpenProfileSection**メソッドは、呼び出し元から情報を読み取るし、可能性のあるアクティブなプロファイルに情報を記述するを有効にすると、プロファイルのセクションを開きます。 
  
クライアントは、 **OpenProfileSection**メソッドを使用してプロバイダーに属するプロファイル セクションを開くことができません。 
  
複数のクライアントまたはサービス プロバイダーでは、読み取り専用のアクセス許可を持つプロファイル セクションを開くことができます同時にします。 ただし、プロファイル セクションが読み取り/書き込み権限で開かれている場合は、他の呼び出しされるアクセスの種類に関係なく、」セクションを開きます。 プロファイル セクションが読み取り専用のアクセス許可で開く場合は、読み取り/書き込みアクセス許可を要求する後続の呼び出しが MAPI_E_NO_ACCESS で失敗します。 同様に、セクションが読み取り/書き込み権限で開かれている場合は、読み取り専用のアクセス許可を要求する後続の呼び出しも失敗します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

要求する場合**OpenProfileSection**は、 _ulFlags_で MAPI_MODIFY を渡すことによってプロファイルが存在しないセクションを開くし、 _lpUID_プロファイルのセクションでは、不明な**MAPIUID**が作成されます。 
  
読み取り専用アクセス権を持つ**OpenProfileSection**が存在しないセクションを開くことを要求した場合は MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI では、 **IProviderAdmin::OpenProfileSection**メソッドを使用して、現在のプロファイルからプロファイルのセクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

