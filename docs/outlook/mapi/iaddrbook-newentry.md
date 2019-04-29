---
title: iaddrbooknewentry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405101"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しい受信者をアドレス帳コンテナーまたは送信メッセージの受信者リストに追加します。
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番ダイアログボックスの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番使用されるテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _cbeidcontainer_
  
> 順番_lpeidcontainer_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lpeidcontainer_
  
> 順番新しい受信者を追加するコンテナーのエントリ識別子へのポインター。 _cbeidcontainer_パラメーターが0の場合、 **newentry**メソッドは、 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md)メソッドが呼び出された場合と同様に、受信者エントリ識別子とテンプレートのリストを返します。 
    
 _cbeidnewentrytpl_
  
> 順番_lpeidnewentrytpl_パラメーターによって指摘されたエントリ識別子のバイト数。 
    
 _lpeidnewentrytpl_
  
> 順番新しい受信者の作成に使用される1回限りのテンプレートへのポインター。 _cbeidnewentrytpl_が0で、 _lpeidnewentrytpl_が NULL の場合、 **newentry**は、ユーザーが新しいエントリを追加するためのテンプレートのリストから選択できるダイアログボックスを表示します。 
    
 _lpcbEIDNewEntry_
  
> 読み上げ_lppeidnewentry_パラメーターによって示されるエントリ識別子のバイト数へのポインター。 
    
 _lppeidnewentry_
  
> 読み上げ新しい受信者のエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいアドレス帳エントリが正常に作成されました。
    
## <a name="remarks"></a>注釈

**newentry**メソッドは、コンテナーに直接追加したり、送信メッセージのアドレス指定に使用したりするために、新しいアドレス帳のエントリを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

新しいエントリを特定のコンテナーに追加する場合は、 _lpeidcontainer_をコンテナーのエントリ id と_cbeidcontainer_に、エントリ識別子のバイト数に設定します。 
  
送信メッセージの受信者一覧に新しいエントリを追加する場合は、 _lpeidcontainer_を NULL に、 _cbeidcontainer_を0に設定します。 
  
クライアントアプリケーションのユーザーが作成するエントリの種類を選択できるようにする場合は、 _lpeidnewentrytpl_で_cbeidnewentrytpl_および NULL に0を渡します。 **newentry**メソッドは、mapi でサポートされているテンプレートの一覧、およびセッション内の各アドレス帳プロバイダーによって mapi の1回限りのテーブルを表示します。 各テンプレートは、1つまたは複数のアドレスの種類の受信者エントリを作成できます。 
  
新しいエントリのエントリ識別子を保持する場合は、 _lpcbEIDNewEntry_および_lppeidnewentry_パラメーターに有効なポインターを渡します。 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことで、このエントリ識別子を解放する責任があります。 
  
特定のテンプレートを使用して、変更可能なコンテナーに新しいエントリを追加するには、次の手順を使用します。
  
1. [imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出して、宛先コンテナーを開き、lな_tryid_パラメーターをコンテナーのエントリ識別子に設定します。 
    
2. 転送先コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、 _ulPropTag_パラメーターを**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に、 _lpiid_パラメーターを IID_IMAPITable に設定します。 コンテナーは、新しいエントリの作成に対してサポートされているすべてのテンプレートを一覧表示する1回限りのテーブルを返します。 
    
3. 作成する特定の種類のエントリのテンプレートを表す行を取得します。 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列は、テンプレートでサポートされているアドレスの種類を示します。
    
4. **newentry**メソッドを呼び出し、 _lpeidnewentrytpl_を、選択したテンプレートのエントリ識別子に設定します。 エントリ id は、1回限りのテーブルのテンプレートの行の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列になります。 _lpeidcontainer_で、 _cbeidcontainer_に0を渡し、NULL を渡します。 新しいエントリのエントリ識別子を保持する場合は、 _lppeidnewentry_パラメーターに有効なポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

