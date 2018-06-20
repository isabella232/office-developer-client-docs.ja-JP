---
title: IAddrBookNewEntry
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800397"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**適用されます**: Outlook 
  
アドレス帳コンテナー、または送信メッセージの受信者の一覧には、新しい受信者を追加します。
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]ダイアログ ボックスの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]使用されるテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _cbEIDContainer_
  
> [in]_LpEIDContainer_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEIDContainer_
  
> [in]新しい受信者を追加するコンテナーのエントリの識別子へのポインター。 _CbEIDContainer_パラメーターが 0 の場合は、 **NewEntry**メソッドは[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドが呼び出された場合と同様の受信者のエントリの識別子と、テンプレートの一覧を返します。 
    
 _cbEIDNewEntryTpl_
  
> [in]_LpEIDNewEntryTpl_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEIDNewEntryTpl_
  
> [in]新しい受信者を作成するために使用する 1 回限りのテンプレートへのポインター。 0、 _cbEIDNewEntryTpl_し、 _lpEIDNewEntryTpl_が NULL の場合、 **NewEntry**は、ユーザーが新しいエントリを追加するためのテンプレートの一覧から選択できますダイアログ ボックスを表示します。 
    
 _lpcbEIDNewEntry_
  
> [out]_LppEIDNewEntry_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEIDNewEntry_
  
> [out]新しい受信者のエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいアドレス帳のエントリが正しく作成されました。
    
## <a name="remarks"></a>備考

**NewEntry**メソッドは、新しいアドレス帳のエントリ、または送信するメッセージに対処するために使用するコンテナーに直接追加するを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

特定のコンテナーに追加する新しいエントリを設定する場合は、コンテナーのエントリの識別子とエントリの識別子のバイト数を_cbEIDContainer_に_lpEIDContainer_を設定します。 
  
送信メッセージの受信者の一覧に追加する新しいエントリを設定する場合は、NULL と 0 を_cbEIDContainer_に_lpEIDContainer_を設定します。 
  
作成するエントリの種類を選択するのにはクライアント アプリケーションのユーザーを許可する場合は、 _cbEIDNewEntryTpl_内の 0 と_lpEIDNewEntryTpl_に NULL を渡します。 **NewEntry**メソッドには、MAPI の一時テーブルでサポートされている MAPI アドレス帳プロバイダーによって、セッションのテンプレートの一覧が表示されます。 各テンプレートには、1 つまたは複数のアドレスの種類の受信者のエントリを作成できます。 
  
新しいエントリのエントリの識別子を保持する場合は、 _lpcbEIDNewEntry_および_lppEIDNewEntry_パラメーターで有効なポインターを渡します。 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって操作を終了したら、このエントリの識別子を解放する責任があります。 
  
変更可能なコンテナーに新しいエントリを追加するのには特定のテンプレートを使用するには、次の手順を使用します。
  
1. 開くには、移動先のコンテナーでは、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すし、コンテナーのエントリの識別子を_lpEntryID_パラメーターを設定します。 
    
2. 、移動先のコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すし、IID_IMAPITable に**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に_ulPropTag_パラメーターは、 _lpiid_パラメーターを設定します。 コンテナーでは、新しいエントリを作成するため、サポートされるすべてのテンプレートを一覧表示する一時テーブルを返します。 
    
3. 特定の種類のエントリを作成するためのテンプレートを表す行を取得します。 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) の列では、テンプレートでサポートされているアドレスの種類を示します。
    
4. **NewEntry**メソッドを呼び出すし、 _lpEIDNewEntryTpl_を選択したテンプレートのエントリの識別子に設定します。 エントリの識別子は、一時テーブル内のテンプレートの行から**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列になります。 _CbEIDContainer_の 0 と_lpEIDContainer_に NULL を渡します。 新しいエントリのエントリの識別子を保持する場合は、 _lppEIDNewEntry_パラメーターに有効なポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[アドレス帳コンテナー](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[PidTagCreateTemplates の標準的なプロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

