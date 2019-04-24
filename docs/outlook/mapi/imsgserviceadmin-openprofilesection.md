---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317399"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
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
  
> プロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpinterface_
  
> 順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lppProfSect_パラメーターで返される標準インターフェイスへのポインターで NULL 値が渡されます。 プロファイルセクションの標準インターフェイスは**IProfSect**です。
    
 _ulFlags_
  
> 順番プロファイルセクションへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し**** 元クライアントがプロファイルセクションを完全に利用できるようになるまで、openprofile の開始を正常に戻すことができます。 プロファイルセクションが使用できない場合は、その後の呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、プロファイルセクションは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを動作させることはできません。 
    
MAPI_FORCE_ACCESS
  
> 個々のサービスプロバイダによって所有されているものも含め、すべてのプロファイルセクションへのアクセスを許可します。
    
 _lppProfSect_
  
> 読み上げプロファイルセクションへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルセクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないプロファイルセクションにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> [要求されたプロファイル] セクションが存在しません。
    
## <a name="remarks"></a>解説

**IMsgServiceAdmin:: openprofile**のメソッドは、プロファイルセクション、 [IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトを開きます。 プロファイルセクションは、セッションプロファイルに関する情報の読み取りおよび書き込みに使用されます。 
  
 **** MAPI_FORCE_ACCESS が使用されていない場合、openprofile を使用して、個々のサービスプロバイダーが所有するプロファイルセクションを開くことはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用アクセス許可でプロファイルセクションを開くことはできますが、読み取り/書き込みアクセス許可を持つプロファイルセクションを開くことができるクライアントは1つだけです。 MAPI_MODIFY フラグセットを使用して openprofile を呼び出すことによっ**** て開こうとして、別のクライアントでプロファイルセクションが開いている場合、呼び出しは失敗し、MAPI_E_NO_ACCESS が返されます。 
  
読み取り専用の開く操作は、セクションが書き込み用に開かれている場合は失敗します。 
  
MAPI_MODIFY フラグと、 _lpuid_パラメーターに存在しない[MAPIUID](mapiuid.md)構造で**openprofile**を呼び出すことで、プロファイルセクションを作成できます。 必ず MAPI_MODIFY を指定してください。 存在しない**MAPIUID**をポイントするように_lpuid_を設定し、 **openプロファイル**が読み取り専用の既定のアクセスモードを使用するように設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> |openプロファイル '  <br/> |mfcmapi は、 **IMsgServiceAdmin:: openprofile**の例を使用して、プロファイルセクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

