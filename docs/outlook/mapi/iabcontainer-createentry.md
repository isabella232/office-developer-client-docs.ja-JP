---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c24adf9f25ab1d8137de76b84b2f612a45b7090e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616951"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザー、配布リスト、または別のコンテナーを指定できる新しいエントリを作成します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子内のバイト数。 
    
 _lpEntryID_
  
> [in]特定の種類の新しいエントリを作成するためのテンプレートのエントリ識別子へのポインター。 
    
 _ulCreateFlags_
  
> [in]エントリの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 重複するエントリチェックの緩いレベルを実行する必要があります。 緩やかな重複エントリチェックの実装は、プロバイダー固有です。 たとえば、プロバイダーは、同じ表示名を持つ任意の 2 つのエントリとして緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 厳密なレベルの重複エントリチェックを実行する必要があります。 厳密な重複エントリチェックの実装は、プロバイダー固有です。 たとえば、プロバイダーは、同じ表示名とメッセージング アドレスの両方を持つ任意の 2 つのエントリとして厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2 つのエントリが重複すると判断された場合は、新しいエントリで既存のエントリが置き換わる必要があります。
    
 _lppMAPIPropEntry_
  
> [out]新しく作成されたエントリへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいエントリが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IABContainer::CreateEntry** メソッドは、指定したコンテナー内の特定の型の新しいエントリを作成し、そのエントリにさらにアクセスするためにインターフェイス実装へのポインターを返します。 新しいエントリは、コンテナーの一時テーブルに公開されている使用可能なテンプレートの一覧から選択されたテンプレートを使用して作成されます。 呼び出し元は [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し、PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することで、コンテナーの **1** 回のテーブルにアクセスします。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IABContainer::CreateEntry** メソッドをサポートするコンテナーはすべて、変更可能である必要があります。 コンテナーの AB_MODIFIABLE **フラグを** PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、変更可能であることを示します。 
  
すべての  _ulCreateFlags フラグをサポートする必要_ があります。 ただし、これらのフラグの解釈と使用は実装固有です。つまり、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のセマンティクスが実装のコンテキストで何を意味するのかを判断できます。 エントリが重複するかどうかを判断できない場合、または決定しない場合は、常にエントリの作成を許可します。 
  
一部のプロバイダーでは、エントリの表示名、メッセージング アドレス、および検索キーを照合して厳密なエントリ チェックを実装します。他のプロバイダーは、一致を表示名とアドレスに制限します。 ルーズ なエントリ チェックは、多くの場合、表示名のみをチェックすることで実装されます。 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>ホスト アドレス帳プロバイダーの実装者へのメモ

コンテナーが他のプロバイダーのテンプレートからエントリを作成できる場合は **、CreateEntry** の実装によって、作成されたエントリに関連付けられたプロパティの一部またはすべてが格納されます。 たとえば、エントリの **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティにストレージを提供する場合、外部プロバイダーに依存することなく詳細ダイアログ ボックスを生成できます。 
  
コンテナーが PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートするエントリを作成できる場合は **、CreateEntry** の実装で次の操作を実行する必要があります。 
  
1. [IMAPISupport::OpenTemplateID メソッドを呼び出](imapisupport-opentemplateid.md)します。 **OpenTemplateID を使用** すると、エントリの外部プロバイダーのコードを作成する新しいエントリにバインドできます。 外部プロバイダーは、このバインド プロセスをサポートして、テンプレートからホスト アドレス帳プロバイダーのコンテナーに作成されたエントリを制御します。 
    
2. 必要な初期化を実行し **、OpenTemplateID** の _lppMAPIPropNew_ パラメーターでオブジェクトが返した外部プロバイダーのエントリのすべてのプロパティを新しいオブジェクトに設定します。
    
**OpenTemplateID** が成功した場合は _、lpMAPIPropData_ パラメーターが指す実装ではなく _、lppMAPIPropNew_ パラメーターが指す実装にプロパティをコピーします。 外部プロバイダーの他のエントリと同様に、オフラインで使用する新しいエントリを初期化します。 
  
**OpenTemplateID がエラー** を返す場合 **、CreateEntry は** 失敗します。 エントリの作成を許可しない。 外部プロバイダーは、プロバイダー内のデータを前提とすることができますので、外部プロバイダーに正常にバインドされていないテンプレート識別子を持つエントリを作成しない。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateEntry が** 返された場合、新しいエントリのエントリ識別子にすぐにアクセスできる場合とアクセスできない場合があります。 一部のアドレス帳プロバイダーでは、新しいエントリの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出すまで使用できません。 
  
重複チェック フラグはパラメーターとして **CreateEntry** に渡されますが **、SaveChanges** が呼び出されるまで、重複チェック操作は実行されません。 したがって、MAPI_E_COLLISION などの関連するエラーは、既に既存のエントリを作成しようとした場合 **、CreateEntry** ではなく **SaveChanges** によって返されます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

