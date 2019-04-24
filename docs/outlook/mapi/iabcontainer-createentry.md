---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287029"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいエントリを作成します。これは、メッセージングユーザー、配布リスト、または別のコンテナーにすることができます。
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番特定の種類の新しいエントリを作成するためのテンプレートのエントリ識別子へのポインター。 
    
 _ulcreateflags_
  
> 順番エントリの作成を実行する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 重複したエントリのチェックは、緩やかなレベルで実行する必要があります。 重複していない重複するエントリのチェックは、プロバイダーに固有のものです。 たとえば、プロバイダーは、同じ表示名を持つ2つのエントリとして緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 重複するエントリの厳密なレベルのチェックを実行する必要があります。 厳密に重複したエントリチェックの実装は、プロバイダーに固有のものです。 たとえば、プロバイダーは、同じ表示名とメッセージアドレスの両方を持つ2つのエントリとして厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2つが重複していると判断された場合は、新しいエントリで既存のエントリを置き換える必要があります。
    
 _lppMAPIPropEntry_
  
> 読み上げ新しく作成されたエントリへのポインターへのポインターを示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいエントリが正常に作成されました。
    
## <a name="remarks"></a>解説

**IABContainer:: createentry**メソッドは、指定されたコンテナーに特定の型の新しいエントリを作成し、そのエントリにさらにアクセスするためのインターフェイス実装へのポインターを返します。 新しいエントリは、1回限りのテーブルで公開されている使用可能なテンプレートの一覧から選択されたテンプレートを使用して作成されます。 発信者は、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することによって、コンテナーの1回限りのテーブルにアクセスします。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IABContainer:: createentry**メソッドをサポートするすべてのコンテナーを変更可能にする必要があります。 コンテナーの AB_MODIFIABLE フラグを**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、それが変更可能であることを示します。 
  
_ulcreateflags_フラグはすべてサポートする必要があります。 ただし、これらのフラグの解釈と使用は実装に固有です。つまり、実装のコンテキストにおける CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT の意味を判断できます。 エントリが重複しているかどうかを判断できない場合、または指定しない場合は、常にエントリの作成を許可します。 
  
プロバイダーによっては、エントリの表示名、メッセージアドレス、および検索キーを一致させることによって、厳密なエントリチェックを実装しています。その他のプロバイダーは、表示名とアドレスに一致するものを制限します。 厳密なエントリチェックは、表示名のみをチェックすることによって実装されることがよくあります。 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>アドレス帳プロバイダー実装者をホストするためのメモ

コンテナーが他のプロバイダーのテンプレートからエントリを作成できる場合は、 **createentry**の実装によって、作成されたエントリに関連付けられているプロパティの一部またはすべてに対してストレージを提供する必要があります。 たとえば、エントリの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティのストレージを提供している場合は、外部プロバイダーに依存せずに [詳細] ダイアログボックスを生成することができます。 
  
コンテナーが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートするエントリを作成できる場合、 **createentry**の実装は次のことを行う必要があります。 
  
1. [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出します。 **OpenTemplateID**では、エントリの外部プロバイダーのコードを使用して、作成される新しいエントリにバインドできます。 外部プロバイダーは、このバインドプロセスをサポートして、テンプレートから作成されたエントリに対する制御をホストアドレス帳プロバイダーのコンテナーに保持します。 
    
2. 必要な初期化を実行し、外部プロバイダーのエントリから、 **OpenTemplateID**から_lppMAPIPropNew_パラメーターで返されるオブジェクトが返されるすべてのプロパティを新しいオブジェクトに設定します。
    
**OpenTemplateID**が正常に終了した場合は、 _lpMAPIPropData_パラメーターで示される実装に直接ではなく、 _lppMAPIPropNew_パラメーターによって示される実装にプロパティをコピーします。 外部プロバイダーからの他のエントリと同様に、オフラインで使用するために新しいエントリを初期化します。 
  
**OpenTemplateID**がエラーを返す場合、 **createentry**は失敗します。 エントリの作成を許可しません。 外部プロバイダーはプロバイダーのデータについて想定することができるので、外部プロバイダーに正常にバインドされていないテンプレート識別子を使用してエントリを作成しないでください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**createentry**から戻ると、新しいエントリのエントリ識別子にすぐにアクセスすることができます。 アドレス帳プロバイダーによっては、新しいエントリの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に使用できなくなります。 
  
重複チェックフラグはパラメーターとして**createentry**に渡されますが、 **SaveChanges**が呼び出されるまで重複したチェック操作は発生しません。 そのため、MAPI_E_COLLISION などの関連エラーは、既に存在するエントリを作成しようとしたことを示しています。これは、 **createentry**ではなく**SaveChanges**によって返されます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

