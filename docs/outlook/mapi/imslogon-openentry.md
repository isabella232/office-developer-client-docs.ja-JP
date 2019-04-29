---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416301"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
folder オブジェクトまたは message オブジェクトを開き、オブジェクトへのポインターを返します。これにより、さらにアクセスできるようになります。 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。 
    
 _lて tryid_
  
> 順番開くフォルダーまたはメッセージオブジェクトのエントリ id のアドレスへのポインター。 
    
 _lpinterface_
  
> 順番オブジェクトのインターフェイス識別子 (IID) へのポインター。 NULL を渡すことは、オブジェクトがそのようなオブジェクトの標準インターフェイスにキャストされることを示します。 _lpinterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子に設定することもできます。 
    
 _ulo・フラグ_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> このオブジェクトは、ユーザーに対して許可されている最大アクセス許可と、クライアントアプリケーションの最大アクセス許可を使用して開かれる必要があります。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可で開かれます。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれます。 クライアントは、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによってアクセス許可レベルを取得できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のオブジェクトが呼び出し元のアプリケーションで使用できない場合でも、呼び出しを成功させることができます。 オブジェクトを使用できない場合は、その後のオブジェクトへの呼び出しでエラーが返されることがあります。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で作成され、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを動作させることはできません。 
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI は**IMSLogon:: openentry**メソッドを呼び出して、メッセージストア内のフォルダーまたはメッセージを開きます。 MAPI は、開くオブジェクトのエントリ識別子に渡されます。 メッセージストアプロバイダーは、 _lppunk_パラメーターで指定されたオブジェクトへのアクセスを可能にするポインターを返す必要があります。 
  
MAPI が**IMSLogon:: openentry**を呼び出す前に、まず、指定されたメッセージまたはフォルダーのエントリ id がこのメッセージストアプロバイダーによって登録されたものと一致することを確認します。 ストアプロバイダーがエントリ識別子を登録する方法の詳細については、「 [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)」を参照してください。
  
 **IMSLogon:: openentry**は、メッセージストアオブジェクトの[IMsgStore:: openentry](imsgstore-openentry.md)メソッドと同じですが、クライアントが**IMSLogon:: openentry**を呼び出さない点が異なります。MAPI は、 **imapisession:: openentry**メソッドを処理するときに**IMSLogon:: openentry**を呼び出します。 **IMSLogon:: openentry**を使用して開いたオブジェクトは、メッセージストアオブジェクトを使用して開かれたオブジェクトとまったく同じように処理される必要があります。特に、メッセージストアオブジェクトが解放されると、この呼び出しを使用して開かれたオブジェクトは無効になります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

