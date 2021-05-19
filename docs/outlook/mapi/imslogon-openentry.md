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
  
フォルダーまたはメッセージ オブジェクトを開き、オブジェクトへのポインターを返して、さらにアクセスできます。 
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _lpEntryID_
  
> [in]開くフォルダーまたはメッセージ オブジェクトのエントリ識別子のアドレスへのポインター。 
    
 _lpInterface_
  
> [in]オブジェクトのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトがそのようなオブジェクトの標準インターフェイスにキャストされます。 _lpInterface パラメーター_ は、オブジェクトの適切なインターフェイスの識別子に設定することもできます。 
    
 _ulOpenFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> オブジェクトは、ユーザーに許可される最大アクセス許可とクライアント アプリケーションの最大アクセス許可で開く必要があります。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可で開きます。クライアントに読み取り専用のアクセス許可がある場合、オブジェクトは読み取り専用のアクセス許可で開きます。 クライアントは、アクセス許可レベルを取得するには、PR_ACCESS_LEVEL **(** [PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のオブジェクトが呼び出し元のアプリケーションで使用できない場合でも、呼び出しは成功できます。 オブジェクトが使用できない場合は、そのオブジェクトに対する後続の呼び出しでエラーが返される可能性があります。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で作成され、クライアントは読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI は **、IMSLogon::OpenEntry** メソッドを呼び出して、メッセージ ストア内のフォルダーまたはメッセージを開きます。 MAPI は、開くオブジェクトのエントリ識別子を渡します。 メッセージ ストア プロバイダーは  _、lppUnk_ パラメーターで指定されたオブジェクトにさらにアクセスできるポインターを返す必要があります。 
  
MAPI が **IMSLogon::OpenEntry** を呼び出す前に、指定されたメッセージまたはフォルダーエントリ識別子が、このメッセージ ストア プロバイダーによって登録された識別子と一致すると最初に判断されます。 ストア プロバイダーがエントリ識別子を登録する方法の詳細については [、「IMAPISupport::SetProviderUID」を参照してください](imapisupport-setprovideruid.md)。
  
 **IMSLogon::OpenEntry** は、クライアントが **IMSLogon::OpenEntry** を呼び出さない以外は、メッセージ ストア オブジェクトの [IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドと同じです。MAPI は **、IMAPISession::OpenEntry** メソッドを処理するときに **IMSLogon::OpenEntry を呼び出** します。 **IMSLogon::OpenEntry** を使用して開くオブジェクトは、メッセージ ストア オブジェクトを使用して開いたオブジェクトとまったく同じように扱う必要があります。特に、この呼び出しを使用して開いたオブジェクトは、メッセージ ストア オブジェクトが解放されると無効になる必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

