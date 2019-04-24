---
title: 外部アドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331211"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>外部アドレス帳プロバイダーとして機能

**適用対象**: Outlook 2013 | Outlook 2016 
  
外部プロバイダーとは、次のようなアドレス帳プロバイダーです。 
  
- 受信者のテンプレート識別子を割り当てます。
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドをサポートします。 
    
- ホストプロバイダーと呼ばれる他のアドレス帳プロバイダーのコンテナーに存在する受信者を管理するためのコードを提供します。 このコードには、property オブジェクト (通常は**imapiprop**インターフェイスの実装) が含まれています。これは、ホストプロバイダーから property オブジェクトをラップします。 
    
外部プロバイダーとして機能するのはオプションの役割です。テンプレート識別子とそれに関連するコードをサポートする必要がないプロバイダーもあります。 プロバイダーから提供されるテンプレートを使用してプロバイダーをホストする受信者の制御を維持する場合は、プロバイダーを外部プロバイダーとして実装します。 
  
プロバイダーがエントリ識別子に使用する形式は、そのテンプレート識別子にも使用できます。 MAPI が受信者を適切なプロバイダーに正しくバインドできるようにするには、テンプレート識別子にプロバイダーの登録済み**MAPIUID**を含める必要があります。 
  
MAPI は、ホストプロバイダーが[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すときに、プロバイダーの**IABLogon:: OpenTemplateID**メソッドを呼び出します。 ホストプロバイダーは、 **imapisupport:: OpenTemplateID**への呼び出しで、受信者のテンプレート識別子を_lpTemplateID_パラメーターに渡します。 MAPI は、テンプレート識別子の[MAPIUID](mapiuid.md)とプロバイダーがログオン時に登録した**MAPIUID**を一致させることによって、テンプレート識別子がプロバイダーに属していると判断します。 その後、MAPI は、 **IABLogon:: OpenTemplateID**メソッドを使用して、ホストプロバイダーの呼び出しをプロバイダーに転送します。 
  
また、ホストプロバイダーは、 _lpMAPIPropData_パラメーターの受信者に対するそのプロパティオブジェクトの実装へのポインターを渡します。 _lpinterface_パラメーターでインターフェイスの実装の種類に対応するインターフェイス識別子です。_lpMAPIPropData_で渡され、省略可能なフラグ FILL_ENTRY。 プロバイダーは、 _lpinterface_で指定された型の property オブジェクト実装へのポインターを_lppMAPIPropNew_パラメータで返すことが想定されています。 返されるポインターは、プロバイダーによって実装されたラップされた property オブジェクト、または_lpMAPIPropData_のホストプロバイダーから提供されたオブジェクトのいずれかになります。 プロバイダーは、次の場合にラップされた property オブジェクトポインターを返します。
  
- 受信者の表示テーブルには、リストボックスコントロールが含まれています。
    
- 受信者の電子メールアドレスは、複数の表示テーブルコントロールのデータからアセンブルする必要があります。
    
- プロバイダーが表示テーブル通知を発行します。
    
FILL_ENTRY フラグは、ホストプロバイダーが受信者のすべてのプロパティを更新する必要があることをプロバイダーに示します。 この要求を満たすには、プロバイダーが必要です。
  
ホストプロバイダーがプロバイダーの**OpenTemplateID**メソッドを呼び出す場合、プロバイダーは次のことを行うことができます。 
  
- コピーしたエントリのデータを定期的に更新します。
    
- コピーしたエントリは、アドレス帳のエントリが個人用アドレス帳にコピーされたときのように、元の値と同期されたままにします。
    
- サーバー上のデータからコピーしたエントリの詳細表にリストボックスを動的に入力するなど、ホストプロバイダーによって実装できない機能を実装します。
    
- コピーしたエントリまたはインスタンス化されたテンプレートで、プロパティ間の相互作用を制御します。 たとえば、[詳細] テーブルに表示されている他のプロパティから**PR_EMAIL_ADDRESS**を計算します。 
    
最初の2つの項目は、ラップされた property オブジェクトを提供する必要がないタスクの例です。これは、ホストプロバイダーの実装に基づく**imapiprop**の実装です。 プロバイダーは単に必要に応じてプロパティを更新し、戻り、ホストプロバイダーによって渡されるポインターをポイントするように_lppMAPIPropNew_パラメーターを_lpMAPIPropData_パラメーターで設定することができます。 
  
2番目の2つのタスクでは、エントリのプロパティシートを表示する機能など、追加機能を持つホストプロバイダーのオブジェクトをラップするプロパティオブジェクトをプロバイダーがホストプロバイダーに返す必要があります。 この property オブジェクトは、 _lpMAPIPropData_パラメータのホストプロバイダによって渡されたオブジェクトの種類に応じて、メッセージのユーザーまたは配布リストのいずれかになります。 _lpinterface_パラメーターのインターフェイス識別子で示されます。 _lpMAPIPropData_パラメーターがメッセージングユーザーを指している場合、プロバイダーのラップされた property オブジェクトは、 **imailuser**の実装である必要があります。 _lpMAPIPropData_が配布リストを指す場合は、 **idistlist**の実装である必要があります。 
  
プロバイダーのラップされた property オブジェクトは、ホストプロバイダーの受信者のコンテキスト固有の操作を実行するために、 **imapiprop**メソッド呼び出しをインターセプトします。これは、ラップしているオブジェクトです。 ラップされた property オブジェクトに MAPI のみが必要です。 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する[imapiprop:: openproperty](imapiprop-openproperty.md)へのすべての呼び出しは、ホストプロバイダーに渡す必要があります。 プロバイダーの実装は、返されたテーブルを使用して、表示テーブル通知を受け取るか、必要に応じて独自に追加することができます。 
  
次の一覧は、通常、外部プロバイダーによって実装されたラップされた property オブジェクトに実装されるタスクを示しています。
  
- [imapiprop:: GetProps](imapiprop-getprops.md)でのホスト受信者の前処理および後処理プロパティの値。
    
- 処理の詳細は、 **imapiprop:: openproperty**で、ボタンやリストボックスなどのテーブルコントロールを表示します。
    
- [imapiprop:: setprops](imapiprop-setprops.md)のホスト受信者のプロパティ値を検証または操作します。
    
- **PR_EMAIL_ADDRESS**などの必要なプロパティを計算し、ホストの受信者を[imapiprop:: SaveChanges](imapiprop-savechanges.md)に保存する前に、必要なすべてのプロパティが設定されていることを確認します。
    
### <a name="to-implement-iablogonopentemplateid"></a>IABLogon:: OpenTemplateID を実装するには
  
1. _lpTemplateID_パラメーターで渡されたテンプレート識別子が有効で、プロバイダーが認識する形式であるかどうかを確認します。 そうでない場合は、失敗して MAPI_E_INVALID_ENTRYID を返します。 
    
2. テンプレート識別子で指定された種類のオブジェクトを作成します。これには、メッセージングユーザー、配布リスト、または1回限りの受信者のいずれかが指定されます。 
    
3. ホストプロバイダーの property オブジェクトで、 _lpMAPIPropData_パラメーターで指定されているオブジェクトである**IUnknown:: AddRef**メソッドを呼び出します。 
    
4. _ultemplateflags_パラメーターが FILL_ENTRY に設定されている場合: 
    
   1. 新しいオブジェクトがメッセージングユーザーまたは配布リストの場合:
      
      1. **imapiprop:: GetProps**メソッドを呼び出すことによって、新しいオブジェクトのすべてのプロパティを取得します。 
          
      2. ホストプロバイダーの**imapiprop:: setprops**メソッドを呼び出して、取得したすべてのプロパティをホストプロバイダーの property オブジェクトにコピーします。 
      
   2. 新しいオブジェクトが1回限りの受信者である場合は、ホストプロバイダーの**imapiprop:: setprops**メソッドを呼び出して、次のプロパティを設定します。 
      
      - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、プロバイダーによって処理されるアドレスの種類を示します。
        
      - **PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) は、 _lpTemplateID_パラメーターおよび_cbTemplateID_パラメーターからテンプレート識別子に対して行います。 
        
      - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) から DT_MAILUSER または DT_DISTLIST に適宜。
    
5. _lppMAPIPropNew_パラメーターの内容を、プロバイダーの新しいオブジェクトまたは_lpMAPIPropData_パラメーターを使用して渡された property オブジェクトのいずれかを指すように設定します。これは、プロバイダーがラップされたオブジェクトを必要とするかどうかによって決まります。 
    
6. ネットワーク障害やメモリ不足の状態などの重大なエラーが発生した場合は、適切なエラー値を返します。 この値は、ホストプロバイダーによって実行されるタスクである適切な[MAPIERROR](mapierror.md)構造を使用して、クライアントに伝達される必要があります。 
    

