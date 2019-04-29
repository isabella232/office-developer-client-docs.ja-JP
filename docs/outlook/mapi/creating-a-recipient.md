---
title: 受信者の作成
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429587"
---
# <a name="creating-a-recipient"></a>受信者の作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、メッセージをアドレス指定するとき、および変更可能なアドレス帳コンテナーにエントリを追加するときに、受信者を作成します。 MAPI には、受信者を作成するための3つの方法があります。
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
メッセージのアドレス指定に使用する受信者を作成する場合は、 **IAddrBook:: createoneoff**を呼び出します。 **createoneoff**は、特定のアドレスの種類のアドレスに関連付けられる特別に書式設定された1回限りのエントリ識別子を作成します。 one-off および一時エントリ識別子の詳細については、「 [1 回限りのアドレス](one-off-addresses.md)と 1 [](one-off-entry-identifiers.md)回限りのエントリ識別子」を参照してください。
  
メッセージのアドレス指定またはコンテナーへの追加のいずれかの受信者を作成する場合は、 **IAddrBook:: newentry**を呼び出します。 **newentry**には、エントリ識別子を含む3つのパラメーターのペアがあります。 これらのパラメーターについては、次のように説明します。 
  
|**パラメーターのペア**|**説明**|
|:-----|:-----|
| _cbeidcontainer_および_lpeidcontainer_ <br/> |新しいエントリが配置されるコンテナーのエントリ識別子。  <br/> |
| _cbeidnewentrytpl_および_lpeidnewentrytpl_ <br/> |新しいエントリを作成するために使用するテンプレートのエントリ識別子。  <br/> |
| _lpcbEidNewEntry_および_lppeidnewentry_ <br/> |新しいエントリのエントリ識別子。  <br/> |
   
送信メッセージの受信者を作成するには、 _cbeidcontainer_をゼロに、 _lpeidcontainer_を NULL に設定します。 **newentry**は、 **IAddrBook:: createoneoff**の呼び出しによって生成されたものと同じ種類の受信者の1回限りの形式に準拠するエントリ識別子を持つ受信者を作成します。 
  
特定のコンテナーに挿入する受信者を作成するには、 _lpeidcontainer_をコンテナーのエントリ識別子と_cbeidcontainer_に、コンテナーのエントリ id のバイト数に設定します。 
  
テンプレートを使用して受信者を作成するには、使用するテンプレートのエントリ識別子に_lpeidnewentrytpl_を設定し、 _cbeidnewentrytpl_をこのエントリ id のバイト数に設定します。 変更可能なアドレス帳コンテナーの多くは、特定の種類のエントリを作成するための1つ以上のテンプレートをサポートしています。 通常、1回限りのテンプレートは、ダイアログボックスの場合がありますが、必ずしもそうではありません。 テンプレートに情報を入力すると、その種類に対して正しく書式設定されたアドレスを持つ受信者が生成されます。 
  
次のいずれかからテンプレートエントリ識別子を取得します。
  
- コンテナーの one-off テーブルの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列。コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) を指定することによってアクセスできます。インターフェイス識別子としてのプロパティタグと IID_IMAPITable。 
    
- プロバイダーのメッセージングユーザーオブジェクトのエントリ識別子を保持するアドレス帳プロバイダーの**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) および**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティ配布リストテンプレート 
    
> [!NOTE]
> 新しいエントリテンプレートのエントリ識別子をテンプレート識別子と呼ばれる別の種類のエントリ識別子と混同しないでください。 テンプレート識別子は、プロバイダーによってのみ使用され、他のプロバイダーからコピーしたエントリを保持します。クライアントによって使用されることはなく、新しいエントリの作成には使用されません。 
  
ユーザーが作成するエントリの種類を決定できるようにするには、 _cbeidnewentrytpl_に0を渡し、 _lpeidnewentrytpl_に対して NULL を渡します。 この場合、 **newentry**は、MAPI の1回限りのテーブルから構築された共通ダイアログボックスを表示します。これには、プロファイル内の各アドレス帳プロバイダーがサポートするすべてのテンプレートの階層的な一覧が表示されます。 
  
アドレスの種類が決定されたときに、 _lpeidnewentrytpl_パラメーターまたは1回限りのテーブル表示からユーザーが選択した項目のいずれかによって、 **newentry**は、その表示テーブルを使用して対応するテンプレートを表示します。 すべての新しいエントリテンプレートは、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートしています。 
  
**newentry**が作成したエントリのエントリ識別子を返すようにするには、 _lpcbEidNewEntry_および_lppeidnewentry_パラメーターの有効なアドレスを渡します。 MAPI は、新しいエントリ識別子を、 _lppeidnewentry_で示されているアドレスと、 _lpcbEidNewEntry_によって示されるアドレスの新しいエントリ識別子のバイト数に配置します。
  
[IABContainer:: createentry](iabcontainer-createentry.md)を呼び出して、受信者を作成し、特定のアドレス帳コンテナーに保存します。 このメソッドは、変更可能なコンテナー ( **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで AB_MODIFIABLE フラグが設定されているコンテナーでのみ使用できます。 この方法は、コンテナーが不変のアドレス帳プロバイダーではサポートされていません。 _lな tryid_パラメーターに、目的の種類のエントリを作成するためのテンプレートのエントリ識別子を指定します。 
  
_ulcreateflags_パラメーターで、必要な重複エントリチェックの種類を指定します。また、新しいエントリで既存のエントリを置き換える必要があるかどうかを指定します。 プロバイダーによってエントリが重複して表示されるために、 **createentry**で新しいオブジェクトの作成に失敗した場合は、エラーまたは警告が返されることを期待しないでください。 このような条件下では、プロバイダーから成功コードが返されます。 
  
コンテナーを直接使用していて、コンテナーが作成できるアドレスの種類が正確にわかっている場合は、 **IABContainer:: createentry**を呼び出して、適切なテンプレートのエントリ識別子を渡すことができます。 アドレス帳プロバイダーは、いくつかの初期の既定のプロパティを設定します。**setprops**を呼び出して他のユーザーを設定することができます。 ユーザーは関与しません。 
  

