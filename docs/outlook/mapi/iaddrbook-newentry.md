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
  
アドレス帳コンテナーまたは送信メッセージの受信者リストに新しい受信者を追加します。
  
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

 _ulUIParam_
  
> [in]ダイアログ ボックスの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]使用するテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _cbEIDContainer_
  
> [in]  _lpEIDContainer_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEIDContainer_
  
> [in]新しい受信者を追加するコンテナーのエントリ識別子へのポインター。 _cbEIDContainer_ パラメーターが 0 の場合 **、NewEntry** メソッドは [、IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドが呼び出された場合と同様に、受信者エントリ識別子とテンプレートのリストを返します。 
    
 _cbEIDNewEntryTpl_
  
> [in]  _lpEIDNewEntryTpl_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEIDNewEntryTpl_
  
> [in]新しい受信者の作成に使用される 1 回きりテンプレートへのポインター。 _cbEIDNewEntryTpl_ がゼロで _lpEIDNewEntryTpl_ が NULL の場合 **、NewEntry** はダイアログ ボックスを表示し、新しいエントリを追加するテンプレートの一覧からユーザーが選択できます。 
    
 _lpcbEIDNewEntry_
  
> [out]  _lppEIDNewEntry_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEIDNewEntry_
  
> [out]新しい受信者のエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいアドレス帳エントリが正常に作成されました。
    
## <a name="remarks"></a>注釈

**NewEntry メソッドは**、新しいアドレス帳エントリを作成し、コンテナーに直接追加するか、送信メッセージのアドレス指定に使用します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

新しいエントリを特定のコンテナーに追加する場合は  _、lpEIDContainer_ をコンテナーのエントリ識別子に設定し  _、cbEIDContainer_ をエントリ識別子のバイト 数に設定します。 
  
送信メッセージの受信者リストに新しいエントリを追加する場合は  _、lpEIDContainer_ を NULL に  _、cbEIDContainer_ を 0 に設定します。 
  
クライアント アプリケーションのユーザーが作成するエントリの種類を選択する場合は _、cbEIDNewEntryTpl で 0、lpEIDNewEntryTpl_ で NULL を渡します。  **NewEntry メソッドは**、MAPI 一時テーブル、MAPI でサポートされているテンプレートの一覧、およびセッション内の各アドレス帳プロバイダーによって表示されます。 各テンプレートは、1 つ以上のアドレスの種類の受信者エントリを作成できます。 
  
新しいエントリのエントリ識別子を保持する場合は  _、lpcbEIDNewEntry_ パラメーターと  _lppEIDNewEntry_ パラメーターに有効なポインターを渡します。 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して終了したら、このエントリ識別子を解放する責任があります。 
  
特定のテンプレートを使用して変更可能なコンテナーに新しいエントリを追加するには、次の手順を使用します。
  
1. [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出して移動先コンテナーを開き _、lpEntryID_ パラメーターをコンテナーのエントリ識別子に設定します。 
    
2. 宛先コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し _、ulPropTag_ パラメーターを PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に _、lpiid_ パラメーターを **IID_IMAPITable** に設定します。 コンテナーは、新しいエントリの作成にサポートしているすべてのテンプレートを一覧表示する 1 回のテーブルを返します。 
    
3. 作成する特定の種類のエントリのテンプレートを表す行を取得します。 **[PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列は、テンプレートでサポートされているアドレスの種類を示します。
    
4. **NewEntry メソッドを呼** び出し _、lpEIDNewEntryTpl_ を選択したテンプレートのエントリ識別子に設定します。 エントリ識別子は、1 回 **PR_ENTRYID** テーブルのテンプレートの行の列 ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列になります。 _cbEIDContainer で 0 を渡し__、lpEIDContainer で NULL を渡します_。 新しいエントリのエントリ識別子を保持する  _場合は、lppEIDNewEntry_ パラメーターに有効なポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

