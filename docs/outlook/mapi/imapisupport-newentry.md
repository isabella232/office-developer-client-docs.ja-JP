---
title: IMAPISupportNewEntry
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d978b7a6bd8af9a505fa025aef2e5da68308468f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588595"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳コンテナーに直接、または送信メッセージの受信者の一覧には、新しい受信者を追加します。
  
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
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbEIDContainer_
  
> [in]_LpEIDContainer_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEIDContainer_
  
> [in]新しいエントリを表示するコンテナーのエントリの識別子へのポインター。 _CbEIDContainer_が 0 で、 _lpEIDContainer_が NULL の場合、 **NewEntry**は、 [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)メソッドの呼び出しによって生成される、同じ種類である 1 回限りのエントリの識別子を作成します。 
    
 _cbEIDNewEntryTpl_
  
> [in]_LpEIDNewEntryTpl_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEIDNewEntryTpl_
  
> [in]使用して新しいエントリを作成するテンプレートのエントリの識別子へのポインター。 **NewEntry**は、 _cbEIDNewEntryTpl_が 0 で、 _lpEIDNewEntryTpl_が NULL の場合、新しいエントリを追加するためのテンプレートの一覧から選択するユーザーを有効にする] ダイアログ ボックスを表示します。 
    
 _lpcbEIDNewEntry_
  
> [out]_LppEIDNewEntry_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEIDNewEntry_
  
> [out]新しく作成したエントリのエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいエントリが正しく作成されました。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::NewEntry**メソッドを実装します。 アドレス帳プロバイダーは、新しいアドレス帳エントリは、コンテナーに直接追加する、送信メッセージに対処するために作成する**NewEntry**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

特定のコンテナーに追加する新しいエントリを設定する場合は、コンテナーのエントリの識別子とエントリの識別子のバイト数を_cbEIDContainer_に_lpEIDContainer_を設定します。 
  
送信メッセージの受信者の一覧に追加する新しいエントリを設定する場合は、NULL と 0 を_cbEIDContainer_に_lpEIDContainer_を設定します。 
  
作成するエントリの種類を選択するのにはクライアント アプリケーションのユーザーを許可する場合は、 _cbEIDNewEntryTpl_内の 0 から_lpEIDNewEntryTpl_に NULL を渡します。 **NewEntry**は、一時テーブルの MAPI、MAPI および各セッションのアドレス帳プロバイダーをサポートするテンプレートの一覧を表示します。 各テンプレートには、1 つまたは複数のアドレスの種類の受信者のエントリを作成できます。 
  
新しいエントリのエントリの識別子を保持する場合は、 _lpcbEIDNewEntry_および_lppEIDNewEntry_パラメーターで有効なポインターを渡します。 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって操作を終了したら、このエントリの識別子を解放する責任があります。 
  
変更可能なコンテナーに新しいエントリを追加するのには特定のテンプレートを使用するには、次の手順を使用します。
  
1. 開くには、移動先のコンテナーでは、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドを呼び出すし、コンテナーのエントリの識別子を_lpEntryID_パラメーターを設定します。 
    
2. 、移動先のコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すし、IID_IMAPITable に**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に_ulPropTag_パラメーターは、 _lpiid_パラメーターを設定します。 コンテナーでは、すべての新しいエントリを作成するためにサポートしているテンプレートの一覧を表示する一時テーブルを返します。 
    
3. 特定の種類のエントリを作成するためのテンプレートを表す行を取得します。 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) の列では、テンプレートでサポートされているアドレスの種類を示します。 
    
4. **IMAPISupport::NewEntry**を呼び出すし、選択したテンプレートのエントリの識別子を_lpEIDNewEntryTpl_パラメーターを設定します。 エントリの識別子は、一時テーブル内のテンプレートの行から**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列です。 _CbEIDContainer_内の 0 から_lpEIDContainer_に NULL を渡します。 新しいエントリのエントリの識別子を保持する場合は、 _lppEIDNewEntry_パラメーターに有効なポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[PidTagCreateTemplates 標準プロパティ Property](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

