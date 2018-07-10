---
title: 外部のアドレス帳プロバイダーとして動作しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16c3518ab4efddbd68765d9de94db64b4fdc0b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799621"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>外部のアドレス帳プロバイダーとして動作しています。

**適用されます**: Outlook 
  
外部のプロバイダーは、アドレス帳プロバイダーです。 
  
- その受信者のテンプレートの識別子を割り当てます。
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドをサポートしています。 
    
- ホスト プロバイダーと呼ばれるその他のアドレス帳のプロバイダーのコンテナー内に存在する受信者を管理するためのコードを提供します。 このコードでは、プロパティ オブジェクト、通常**IMAPIProp**インターフェイスの実装、ホスト プロバイダーからのプロパティのオブジェクトをラップする必要があります。 
    
外部のプロバイダーとしての機能は、オプションの役割です。すべてのプロバイダーでは、テンプレートの識別子と、関連するコードをサポートする必要があります。 ホスト プロバイダーは、プロバイダーから提供されたテンプレートを使用するを作成する受信者の管理を維持する場合は、外部プロバイダーとしてプロバイダーを実装します。 
  
エントリ id は、プロバイダーを使用する形式は、そのテンプレートの識別子も使用できます。 テンプレート識別子には、正常に受信者を適切なプロバイダーにバインドするための MAPI を有効にするのには、プロバイダーの登録されている**MAPIUID**を含める必要があります。 
  
MAPI では、ホスト プロバイダーの呼び出し[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)するときに、プロバイダーの**IABLogon::OpenTemplateID**メソッドを呼び出します。 ホスト プロバイダーは、 **IMAPISupport::OpenTemplateID**への呼び出し内の_lpTemplateID_パラメーターで、受信者のテンプレートの識別子を渡します。 MAPI では、テンプレートの識別子が、 [MAPIUID](mapiuid.md)テンプレート id でログオン時に、プロバイダーが登録されている**MAPIUID**とを照合することによって、プロバイダーに属しているを決定します。 MAPI は、 **IABLogon::OpenTemplateID**メソッドを使用し、プロバイダーのホスト プロバイダーの呼び出しを転送します。 
  
ホスト プロバイダーもポインターを渡します、プロパティ オブジェクトの実装に、 _lpMAPIPropData_パラメーター内の受信者、インターフェイスの実装の種類に対応する_lpInterface_パラメーターにインターフェイス識別子_lpMAPIPropData_、およびオプションのフラグ、FILL_ENTRY に渡されます。 プロバイダーは、 _lpInterface_で指定された型のプロパティ オブジェクトの実装に_lppMAPIPropNew_パラメーターにポインターを返す必要があります。 返されたポインターできる、プロバイダーによって実装されているプロパティをラップされたオブジェクトにまたは_lpMAPIPropData_のホスト プロバイダーから提供されたオブジェクトにします。 プロバイダーがプロパティをラップされたオブジェクトのポインターを返す必要がある場合。
  
- 受信者の表示のテーブルには、リスト ボックス コントロールが含まれています。
    
- 受信者の電子メール アドレスは、複数のディスプレイ テーブル コントロール内のデータで組み立てられる必要があります。
    
- プロバイダーの問題では、テーブルの通知を表示します。
    
FILL_ENTRY フラグは、ホスト プロバイダーを更新する受信者のすべてのプロパティが必要である、プロバイダーに指示します。 プロバイダーは、この要求を満たすために必要です。
  
ホスト プロバイダーが、プロバイダーの**OpenTemplateID**メソッドを呼び出すと、プロバイダー可能性があります。 
  
- コピーしたエントリのデータを定期的に更新します。
    
- コピーしたエントリが個人用アドレス帳にアドレス帳エントリをコピーするときなど、元と同期してください。
    
- サーバー上のデータからコピーしたエントリの詳細の表でボックスの実装の機能リストを動的に生成するなど、ホスト プロバイダーが実装することはできません。
    
- コピーしたエントリまたはインスタンス化されたテンプレートのプロパティ間の相互作用を制御します。 [明細] テーブルに表示されるその他のプロパティから、たとえば、 **PR_EMAIL_ADDRESS**を計算しています。 
    
プロパティをラップされたオブジェクトを指定するのには、プロバイダーを必要としないタスクの例としては、最初の 2 つの項目、ホスト プロバイダーの実装に基づく**IMAPIProp**を実装します。 プロバイダーは、必要に応じて、戻り値、 _lpMAPIPropData_パラメーターでは、ホスト プロバイダーから渡されたポインターを指すように_lppMAPIPropNew_パラメーターを設定するとプロパティを更新できますだけです。 
  
2 つ目は 2 つのタスクでは、エントリのプロパティ シートを表示する機能などの追加機能によって、ホスト プロバイダーのオブジェクトをラップするプロパティ オブジェクトのホスト プロバイダーには、プロバイダーが返す必要があります。 このプロパティ オブジェクトはメッセージのユーザーまたは配布リスト、 _lpMAPIPropData_パラメーターでは、ホスト プロバイダーによって渡される_lpInterface_パラメーターにインターフェイス識別子で指定されたオブジェクトの種類に応じて。 _LpMAPIPropData_パラメーターは、メッセージングのユーザーをポイントしている場合、プロバイダーのプロパティをラップされたオブジェクトは、 **IMailUser**実装をする必要があります。 _LpMAPIPropData_は、配布リストをポイントしている場合、 **IDistList**の実装があります。 
  
**IMAPIProp**ホスト プロバイダーの受信者のコンテキストに固有の操作を実行するメソッドの呼び出しをインターセプトする、プロバイダーのプロパティをラップされたオブジェクトのそれをラップするオブジェクト。 MAPI では、オブジェクトの折り返しが設定されたプロパティの要件の 1 つだけは、: [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するすべての呼び出しは、ホスト プロバイダーに渡す必要があります。 プロバイダーの実装は、表示テーブルの通知を受け取るかに応じて、独自に追加するのには、返されるテーブルを使用できます。 
  
次の一覧には、外部プロバイダーによって実装されるプロパティをラップされたオブジェクトの実装は、通常のタスクが含まれています。
  
- 前処理スクリプトと[IMAPIProp::GetProps](imapiprop-getprops.md)のホストの受信者のプロパティの値を後処理します。
    
- 処理の詳細は、 **IMAPIProp::OpenProperty**のボタンやリスト ボックスなど、テーブルのコントロールを表示します。
    
- 検証または[IMAPIProp::SetProps](imapiprop-setprops.md)でホストの受信者のプロパティの値を操作します。
    
- **PR_EMAIL_ADDRESS**などの必要なプロパティを計算し、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)でホストの受信者を保存する前に設定されているすべての必要なプロパティを確認します。
    
### <a name="to-implement-iablogonopentemplateid"></a>IABLogon::OpenTemplateID を実装するには
  
1. テンプレート識別子が渡された場合、 _lpTemplateID_パラメーターが有効なでは、プロバイダーで認識される形式でを確認します。 そうでない場合は失敗し、MAPI_E_INVALID_ENTRYID を返します。 
    
2. テンプレート識別子で指定された型のオブジェクトを作成するメッセージングのユーザー、配布リスト、または 1 回限りの受信者のいずれかです。 
    
3. ホスト プロバイダーのプロパティ オブジェクトは、 _lpMAPIPropData_パラメーターが指すオブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
    
4. 場合は、 _ulTemplateFlags_パラメーターを FILL_ENTRY に設定するとします。 
    
   1. 新しいオブジェクトがメッセージのユーザーまたは配布リストの場合。
      
      1. すべてを取得、新しいオブジェクトのプロパティの可能性があります、 **IMAPIProp::GetProps**メソッドを呼び出してください。 
          
      2. ホスト プロバイダーのプロパティ オブジェクトを取得したプロパティのすべてをコピーするのには、ホスト プロバイダーの**IMAPIProp::SetProps**メソッドを呼び出します。 
      
   2. 新しいオブジェクトが 1 回限りの受信者の場合は、次のプロパティを設定するのには、ホスト プロバイダーの**IMAPIProp::SetProps**メソッドを呼び出します。 
      
      - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、プロバイダーによって処理されるアドレスの種類にします。
        
      - **PR\_テンプレート ID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))、 _lpTemplateID_および_cbTemplateID_パラメーターからテンプレート識別子にします。 
        
      - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER または DT_DISTLIST では、必要に応じてします。
    
5. プロバイダーの新しいオブジェクトまたはいずれかが必要で、ラップされたオブジェクトをプロバイダーが判断するかどうかに応じて、 _lpMAPIPropData_パラメーターで渡されたプロパティのオブジェクトを指すように_lppMAPIPropNew_パラメーターの内容を設定します。 
    
6. ネットワーク障害や、メモリ不足の状態などの重大なエラーが発生した場合は、適切なエラー値を返します。 この値の適切な[MAPIERROR](mapierror.md)構造体、ホスト プロバイダーによって実行されるタスクをクライアントに反映される必要があります。 
    
