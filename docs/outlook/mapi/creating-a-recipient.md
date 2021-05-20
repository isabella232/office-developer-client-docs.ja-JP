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
  
クライアントは、メッセージへのアドレス指定時、および変更可能なアドレス帳コンテナーにエントリを追加するときに受信者を作成します。 MAPI には、受信者を作成するための 3 つの方法があります。
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
メッセージ **のアドレス指定に使用する受信者を作成するときに、IAddrBook::CreateOneOff** を呼び出します。 **CreateOneOff** は、特定のアドレスの種類のアドレスに関連付けられる、特別に書式設定された 1 回限定のエントリ識別子を作成します。 1 回きりと 1 回のエントリ識別子の詳細については [、「One-Off Addresses](one-off-addresses.md) and [One-Off Entry IDENTIFIERs」を参照してください](one-off-entry-identifiers.md)。
  
メッセージのアドレス指定またはコンテナーへの追加に使用する受信者を作成する場合は **、IAddrBook::NewEntry** を呼び出します。 **NewEntry には** 、エントリ識別子を含む 3 組のパラメーターがあります。 これらのパラメーターについては、次のように説明します。 
  
|**パラメーターのペア**|**説明**|
|:-----|:-----|
| _cbEidContainer と_  _lpEidContainer_ <br/> |新しいエントリを配置するコンテナーのエントリ識別子。  <br/> |
| _cbEidNewEntryTpl と_  _lpEidNewEntryTpl_ <br/> |新しいエントリの作成に使用するテンプレートのエントリ識別子。  <br/> |
| _lpcbEidNewEntry と_  _lppEidNewEntry_ <br/> |新しいエントリのエントリ識別子。  <br/> |
   
送信メッセージの受信者を作成するには  _、cbEidContainer_ を 0 に  _、lpEidContainer_ を NULL に設定します。 **NewEntry は****、IAddrBook::CreateOneOff** の呼び出しによって生成される受信者と同じ種類の 1 回の形式に準拠するエントリ識別子を持つ受信者を作成します。 
  
特定のコンテナーに挿入する受信者を作成するには  _、lpEidContainer_ をコンテナーのエントリ識別子に  _、cbEidContainer_ をコンテナーのエントリ識別子のバイト数に設定します。 
  
テンプレートを使用して受信者を作成するには  _、lpEidNewEntryTpl_ を使用するテンプレートのエントリ識別子  _、cbEidNewEntryTpl_ をこのエントリ識別子のバイト数に設定します。 ほとんどの変更可能なアドレス帳コンテナーは、特定の種類のエントリを作成するための 1 つ以上のテンプレートをサポートします。 通常、1 回限りテンプレートはダイアログ ボックスですが、必ずしもそうではありません。 テンプレートに情報を入力すると、型の形式が正しいアドレスを持つ受信者が生成されます。 
  
次のいずれかの方法でテンプレートエントリ識別子を取得します。
  
- コンテナー **の 1** 回限りテーブルの **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)列は、コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し、PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) をプロパティ タグとして、IID_IMAPITable をインターフェイス識別子として指定してアクセスします。 
    
- プロバイダーのメッセージング ユーザー オブジェクトおよび配布リスト テンプレートのエントリ識別子を保持するアドレス帳プロバイダーの **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) プロパティと **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティ。 
    
> [!NOTE]
> 新しいエントリ テンプレートのエントリ識別子と、テンプレート識別子と呼ばれる別の種類のエントリ識別子を混同しない。 テンプレート識別子は、他のプロバイダーからコピーされたエントリを維持するためにプロバイダーによってのみ使用されます。クライアントでは使用されません。新しいエントリの作成には使用されません。 
  
ユーザーが作成するエントリの種類を決定するには  _、cbEidNewEntryTpl に 0、lpEidNewEntryTpl_ に NULL を  _渡します_。 この場合 **、NewEntry** は MAPI の一時テーブルから構築された共通のダイアログ ボックスを表示します。プロファイル内の各アドレス帳プロバイダーでサポートされるテンプレートの階層リストです。 
  
アドレスの種類が決定された場合は  _、lpEidNewEntryTpl_ パラメーターの設定、または一時テーブル表示からのユーザーによる選択のいずれかによって **、NewEntry** は対応するテンプレートを表示テーブルを使用して表示します。 すべての新しいエントリ テンプレートは **、PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートします。 
  
**NewEntry** に作成されたエントリのエントリ識別子を返す場合は _、lpcbEidNewEntry_ パラメーターと _lppEidNewEntry_ パラメーターの有効なアドレスを渡します。 MAPI は  _、lppEidNewEntry_ が指すアドレスに新しいエントリ識別子を、新しいエントリ識別子のバイト 数を  _lpcbEidNewEntry_ が指すアドレスに格納します。
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)を呼び出して受信者を作成し、それを特定のアドレス帳コンテナーに保存します。 このメソッドは、PR_CONTAINER_FLAGS **(** [PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに AB_MODIFIABLE フラグが設定されている変更可能なコンテナーでのみ使用できます。 変更できないコンテナーを持つアドレス帳プロバイダーでは、このメソッドはサポートされていません。 _lpEntryID_ パラメーターに目的の型のエントリを作成するためのテンプレートのエントリ識別子を指定します。 
  
_ulCreateFlags_ パラメーターで、必要な重複エントリチェックの種類と、新しいエントリが既存のエントリを置き換えるかどうかを指定します。 **CreateEntry が** プロバイダーによって課せられた重複するエントリチェックのために新しいオブジェクトを作成できない場合は、エラーまたは警告が返されるのを期待しません。 これらの条件では、プロバイダーは成功コードを返します。 
  
コンテナーを直接操作し、コンテナーが作成できるアドレスの種類を正確に把握している場合は **、IABContainer::CreateEntry** を呼び出して、適切なテンプレートのエントリ識別子を渡します。 アドレス帳プロバイダーは、初期の既定のプロパティを設定します。 **SetProps を呼び出して他** のユーザーを設定できます。 ユーザーは関与しない。 
  

