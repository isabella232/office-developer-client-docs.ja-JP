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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800354"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**適用対象**: Outlook 
  
メッセージングのユーザー、配布リスト、または別のコンテナーにすることができますが、新しいエントリを作成します。
  
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子内のバイト数。 
    
 _lpEntryID_
  
> [in]特定の種類の新しいエントリを作成するためのテンプレートのエントリの識別子へのポインター。 
    
 _ulCreateFlags_
  
> [in]エントリの作成を実行する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 緩やかなレベルの重複するエントリのチェックを実行する必要があります。 緩やかな重複するエントリのチェックの実装は、特定のプロバイダーです。 などのプロバイダーは、同じ 2 つのエントリの表示名と緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 厳密なレベルの重複するエントリのチェックを実行する必要があります。 厳密な重複するエントリのチェックの実装は、特定のプロバイダーです。 などのプロバイダーは、両方同じ 2 つのエントリの名前とメッセージのアドレスを表示すると、厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2 つ重複していることが判明した場合、新しいエントリは既存のものに置き換えてください。
    
 _lppMAPIPropEntry_
  
> [out]新しく作成されたエントリへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいエントリが正しく作成されました。
    
## <a name="remarks"></a>注釈

**IABContainer::CreateEntry**メソッドは、インターフェイスの実装のエントリにさらにアクセスするためにポインターを返す、指定したコンテナーに特定の種類の新しいエントリを作成します。 新しいエントリを作成するには、その一時テーブルで公開されている、利用可能なテンプレートのコンテナーの一覧から選択されているテンプレートを使用します。 呼び出し元の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを要求しているコンテナーの一時テーブルにアクセスします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**IABContainer::CreateEntry**メソッドをサポートするすべてのコンテナーは、変更可能である必要があります。 変更可能であることを示すには、その**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで、コンテナーの AB_MODIFIABLE フラグを設定します。 
  
_UlCreateFlags_フラグをすべてサポートする必要があります。 ただし、解釈し、これらのフラグの使用は、特定の実装-は、実装のコンテキストで意味する CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT の意味を判断できます。 できないかのエントリは、重複しているかどうかを判断できませんを作成するエントリを常に許可します。 
  
プロバイダーによって実装厳密なエントリの表示名を照合することによってチェックがメッセージング アドレス、および検索キーのエントリです。他のプロバイダーでは、名前とアドレスを表示するのには一致するものを制限します。 緩やかなエントリのチェックは、多くの場合のみの表示名を確認することによって実装されます。 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>アドレス帳プロバイダーの実装をホストするためのメモ

コンテナーは、他のプロバイダーのテンプレートの中から、エントリを作成できます、 **CreateEntry**の実装は、作成されたエントリに関連付けられているプロパティの一部またはすべてのストレージを提供する必要があります。 などのエントリの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティの記憶域を提供する場合は、外部プロバイダーに依存することがなくその [詳細] ダイアログ ボックスを生成できます。 
  
コンテナーには、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートするためのエントリを作成できます、 **CreateEntry**の実装が、次の操作にする必要があります。 
  
1. [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出します。 **OpenTemplateID**は、外部プロバイダーのエントリが作成される新しいエントリにバインドするコードを有効にします。 外部プロバイダーでは、ホストのアドレス帳プロバイダーのコンテナー内にそのテンプレートから作成されたエントリの制御を維持するには、このバインド処理をサポートします。 
    
2. 、必要な初期化を実行し、新しいオブジェクトにすべての**OpenTemplateID**から、 _lppMAPIPropNew_パラメーターで返されるオブジェクトを外部のプロバイダーのエントリからプロパティを設定します。
    
**OpenTemplateID**が成功した場合は、 _lpMAPIPropData_パラメーターで指定された実装に直接ではなく、 _lppMAPIPropNew_パラメーターで指定された実装にプロパティをコピーします。 外部プロバイダーから他の任意のエントリを同じように、オフラインで使用する新しいエントリを初期化します。 
  
**OpenTemplateID**には、エラーが返されます、 **CreateEntry**が失敗する必要があります。 作成するエントリを許可しません。 外部のプロバイダーは、プロバイダーで、データに関する判断を行うことができます、ために、外部のプロバイダーに正常にバインドされていないいるテンプレート識別子を持つエントリは作成できません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateEntry**が返されるときにする、新しいエントリのエントリ id をすぐにアクセスできない場合があります。 アドレス帳のプロバイダーによって、それはないまで利用可能な新しいエントリの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後。 
  
重複チェック フラグは、 **CreateEntry**にパラメーターとして渡されます、ただし、 **SaveChanges**が呼び出されるまで操作を確認した後、複製は発生しません。 したがって、 **CreateEntry**ではなく、**たいていは SaveChanges**は、既に既存のエントリを作成しようとすることを示す、MAPI_E_COLLISION などの関連するエラーが返されます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates 標準プロパティ Property](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

