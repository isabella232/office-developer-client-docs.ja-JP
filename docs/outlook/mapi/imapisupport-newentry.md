---
title: imapisupportnewentry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316645"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーまたは送信メッセージの受信者リストに、新しい受信者を直接追加します。
  
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
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbeidcontainer_
  
> 順番_lpeidcontainer_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lpeidcontainer_
  
> 順番新しいエントリを受け取るコンテナーのエントリ識別子へのポインター。 _cbeidcontainer_が0で_lpeidcontainer_が NULL の場合、 **newentry**は、 [imapisupport:: createoneoff](imapisupport-createoneoff.md)メソッドへの呼び出しによって生成されたものと同じ種類の1回限りのエントリ id を作成します。 
    
 _cbeidnewentrytpl_
  
> 順番_lpeidnewentrytpl_パラメーターによって指摘されたエントリ識別子のバイト数。 
    
 _lpeidnewentrytpl_
  
> 順番新しいエントリを作成するために使用するテンプレートのエントリ識別子へのポインター。 _cbeidnewentrytpl_が0で、 _lpeidnewentrytpl_が NULL の場合、 **newentry**はダイアログボックスを表示して、ユーザーが新しいエントリを追加するためにテンプレートのリストから選択できるようにします。 
    
 _lpcbEIDNewEntry_
  
> 読み上げ_lppeidnewentry_パラメーターによって示されるエントリ識別子のバイト数へのポインター。 
    
 _lppeidnewentry_
  
> 読み上げ新しく作成されたエントリのエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいエントリが正常に作成されました。
    
## <a name="remarks"></a>解説

アドレス帳プロバイダーサポートオブジェクトには、 **imapisupport:: newentry**メソッドが実装されています。 アドレス帳プロバイダーは**** 、新しいアドレス帳エントリを作成してコンテナーに直接追加したり、送信メッセージのアドレス指定に使用したりします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

新しいエントリを特定のコンテナーに追加する場合は、 _lpeidcontainer_をコンテナーのエントリ id と_cbeidcontainer_に、エントリ識別子のバイト数に設定します。 
  
送信メッセージの受信者一覧に新しいエントリを追加する場合は、 _lpeidcontainer_を NULL に、 _cbeidcontainer_を0に設定します。 
  
クライアントアプリケーションのユーザーが作成するエントリの種類を選択できるようにする場合は、 _cbeidnewentrytpl_では0を、 _lpeidnewentrytpl_では NULL を渡します。 **newentry**は、mapi の1回限りのテーブル (mapi と、セッションでサポートされている各アドレス帳プロバイダー) の一覧を表示します。 各テンプレートは、1つまたは複数のアドレスの種類の受信者エントリを作成できます。 
  
新しいエントリのエントリ識別子を保持する場合は、 _lpcbEIDNewEntry_および_lppeidnewentry_パラメーターに有効なポインターを渡します。 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことで、このエントリ識別子を解放する責任があります。 
  
特定のテンプレートを使用して、変更可能なコンテナーに新しいエントリを追加するには、次の手順を使用します。
  
1. [imapisupport:: openentry](imapisupport-openentry.md)メソッドを呼び出して、宛先コンテナーを開き、lな_tryid_パラメーターをコンテナーのエントリ識別子に設定します。 
    
2. 転送先コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、 _ulPropTag_パラメーターを**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に、 _lpiid_パラメーターを IID_IMAPITable に設定します。 コンテナーは、新しいエントリを作成するためにサポートされているすべてのテンプレートを一覧表示する1回限りのテーブルを返します。 
    
3. 作成する特定の種類のエントリのテンプレートを表す行を取得します。 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列は、テンプレートでサポートされているアドレスの種類を示します。 
    
4. **imapisupport:: newentry**を呼び出し、 _lpeidnewentrytpl_パラメーターを、選択したテンプレートのエントリ識別子に設定します。 エントリ識別子は、1回限りのテーブルのテンプレートの行の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列です。 _lpeidcontainer_で、 _cbeidcontainer_に0を渡し、NULL を渡します。 新しいエントリのエントリ識別子を保持する場合は、 _lppeidnewentry_パラメーターに有効なポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

