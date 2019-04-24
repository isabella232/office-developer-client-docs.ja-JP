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
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301548"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルからプロファイルセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番開くプロファイルセクションの一意識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 クライアントは_lpuid_パラメーターに NULL を渡すことはできません。 サービスプロバイダーは、メッセージサービスのエントリポイント関数から呼び出したときに、 **MAPIUID**を取得するために NULL を渡すことができます。 
    
 _lpinterface_
  
> 順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL 結果をプロファイルセクションの標準インターフェイス (**IProfSect**) に渡すと、返されます。 
    
 _ulFlags_
  
> 順番プロファイルセクションが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元がプロファイルセクションを完全に利用できるようになる前に、 **openプロファイル**を正常に返すことができるようにします。 プロファイルセクションが使用できない場合は、その後の呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。 クライアントは、プロファイルのプロバイダーセクションに対する読み取り/書き込みアクセス許可を許可しません。
    
MAPI_FORCE_ACCESS
  
> 個々のサービスプロバイダによって所有されているものも含め、すべてのプロファイルセクションへのアクセスを許可します。
    
 _lppProfSect_
  
> 読み上げプロファイルセクションへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルセクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用プロファイルセクションを変更しようとしたか、またはユーザーが十分な権限を持っていないオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> [要求されたプロファイル] セクションが存在しません。
    
## <a name="remarks"></a>解説

**IProviderAdmin:: openprofile**のメソッドは、プロファイルセクションを開き、発信者が情報を読み取り、アクティブなプロファイルに情報を書き込むことができるようにします。 
  
クライアントは、openプロファイルの使い方を使用して、 **** プロバイダーに属するプロファイルセクションを開くことができません。 
  
複数のクライアントまたはサービスプロバイダーは、読み取り専用のアクセス許可を持つプロファイルセクションを同時に開くことができます。 ただし、プロファイルセクションが読み取り/書き込みアクセス許可で開かれている場合、アクセスの種類に関係なく、セクションを開く他の呼び出しを行うことはできません。 読み取り専用アクセス許可でプロファイルセクションが開かれている場合、読み取り/書き込みアクセス許可を要求する後続の呼び出しは、MAPI_E_NO_ACCESS で失敗します。 同様に、セクションが読み取り/書き込みアクセス許可で開かれている場合は、読み取り専用アクセス許可を要求する次の呼び出しも失敗します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIUID**で MAPI_MODIFY を渡すことによって、存在しないプロファイルセクションを__ 開くように**openprofile**を要求__ した場合は、[プロファイル] セクションが作成されます。 
  
読み取り専用アクセス許可で、存在しないセクションを開くように**openプロファイル**を要求すると、MAPI_E_NOT_FOUND が返されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> |openプロファイル '  <br/> |mfcmapi は、 **IProviderAdmin:: openprofile**の例を使用して、現在のプロファイルからプロファイルセクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

