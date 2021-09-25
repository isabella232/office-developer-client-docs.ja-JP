---
title: 外部アドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c72269d09e4b14f86e08a848084645aca7f6ca61
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567922"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>外部アドレス帳プロバイダーとして機能

**適用対象**: Outlook 2013 | Outlook 2016 
  
外部プロバイダーは、次のようなアドレス帳プロバイダーです。 
  
- 受信者のテンプレート識別子を割り当てる。
    
- [IABLogon::OpenTemplateID メソッドをサポート](iablogon-opentemplateid.md)します。 
    
- ホスト プロバイダーと呼ばれる他のアドレス帳プロバイダーのコンテナーに存在する受信者を維持するためのコードを提供します。 このコードには、ホスト プロバイダーからプロパティ オブジェクトをラップするプロパティ オブジェクト ( **通常は IMAPIProp** インターフェイス実装) が含まれる。 
    
外部プロバイダーとしての役割はオプションの役割です。すべてのプロバイダーがテンプレート識別子とその関連コードをサポートする必要はありません。 プロバイダーによって提供されるテンプレートを使用してホスト プロバイダーが作成する受信者に対する制御を維持する場合は、プロバイダーを外部プロバイダーとして実装します。 
  
プロバイダーがエントリ識別子に使用する形式は、テンプレート識別子にも使用できます。 MAPI が適切なプロバイダーに受信者を正常にバインドするには、テンプレート識別子にプロバイダーの登録済み **MAPIUID** が含まれる必要があります。 
  
MAPI は、ホスト プロバイダーが [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出す場合に、プロバイダーの **IABLogon::OpenTemplateID** メソッドを呼び出します。 ホスト プロバイダーは **、IMAPISupport::OpenTemplateID** を呼び出す _lpTemplateID_ パラメーター内の受信者のテンプレート識別子を渡します。 MAPI は、テンプレート識別子の [MAPIUID](mapiuid.md) を、ログオン時にプロバイダーが登録した **MAPIUID** と照合することで、テンプレート識別子がプロバイダーに属すると判断します。 MAPI は **、IABLogon::OpenTemplateID** メソッドを使用してホスト プロバイダーの呼び出しをプロバイダーに転送します。 
  
ホスト プロバイダーは _、lpMAPIPropData_ パラメーターの受信者のプロパティ オブジェクト実装へのポインター _、lpMAPIPropData_ で渡されるインターフェイス実装の種類に対応する _lpInterface_ パラメーターのインターフェイス識別子、およびオプションのフラグ FILL_ENTRY を渡します。 プロバイダーは  _、lppMAPIPropNew_ パラメーターに lpInterface で指定された型のプロパティ オブジェクト実装へのポインター  _を返す必要があります_。 返されるポインターは、プロバイダーによって実装されたラップされたプロパティ オブジェクト、または  _lpMAPIPropData_ のホスト プロバイダーによって提供されるオブジェクトのいずれかです。 プロバイダーは、次の場合にラップされたプロパティ オブジェクト ポインターを返す必要があります。
  
- 受信者の表示テーブルには、リスト ボックス コントロールが含まれています。
    
- 受信者の電子メール アドレスは、複数の表示テーブル コントロールのデータから組み立てる必要があります。
    
- プロバイダーは、表示テーブル通知を発行します。
    
[FILL_ENTRY] フラグは、ホスト プロバイダーが受信者のすべてのプロパティを更新する必要があるというメッセージをプロバイダーに示します。 プロバイダーは、この要求を満たす必要があります。
  
ホスト プロバイダーがプロバイダーの **OpenTemplateID** メソッドを呼び出す場合、プロバイダーは次の場合があります。 
  
- コピーされたエントリのデータを定期的に更新します。
    
- コピーされたエントリを、アドレス帳エントリが個人用アドレス帳にコピーされる場合など、元のエントリと同期された状態に保つ。
    
- サーバー上のデータからコピーされたエントリの詳細テーブルにリスト ボックスを動的に設定するなど、ホスト プロバイダーが実装できない機能を実装します。
    
- コピーされたエントリまたはインスタンス化されたテンプレート内のプロパティ間の相互作用を制御します。 たとえば、詳細テーブル **PR_EMAIL_ADDRESS** 他のプロパティからデータを計算します。 
    
最初の 2 つの項目は、プロバイダーがラップされたプロパティ オブジェクト (ホスト プロバイダーの実装に基づく **IMAPIProp** の実装) を提供する必要としないタスクの例です。 プロバイダーは、必要に応じてプロパティを更新して返すだけで  _、lppMAPIPropNew_ パラメーターを  _lpMAPIPropData_ パラメーターでホスト プロバイダーが渡すポインターをポイントする設定を行います。 
  
2 番目の 2 つのタスクでは、プロバイダーがホスト プロバイダーに戻り、ホスト プロバイダーのオブジェクトを折り返すプロパティ オブジェクト (エントリのプロパティ シートを表示する機能など) を追加する必要があります。 このプロパティ オブジェクトは  _、lpMAPIPropData_ パラメーターでホスト プロバイダーによって渡され  _、lpInterface_ パラメーターのインターフェイス識別子によって示されるオブジェクトの種類に応じて、メッセージング ユーザーまたは配布リストになります。 _lpMAPIPropData_ パラメーターがメッセージング ユーザーをポイントする場合、プロバイダーのラップされたプロパティ オブジェクトは **IMailUser 実装である必要** があります。 _lpMAPIPropData が_ 配布リストをポイントする場合は **、IDistList 実装である必要** があります。 
  
プロバイダーのラップされたプロパティ オブジェクトは **、IMAPIProp** メソッドの呼び出しをインターセプトして、ホスト プロバイダーの受信者 (ラップしているオブジェクト) のコンテキスト固有の操作を実行します。 MAPI には、ラップされたプロパティ オブジェクトの要件が **1** つのみです。PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する [IMAPIProp::OpenProperty](imapiprop-openproperty.md)へのすべての呼び出しをホスト プロバイダーに渡す必要があります。 プロバイダーの実装では、返されるテーブルを使用して、表示テーブルの通知を傍受したり、必要に応じて独自の通知を追加することができます。 
  
次の一覧には、外部プロバイダーによって実装されるラップされたプロパティ オブジェクトに通常実装されるタスクが含まれています。
  
- [IMAPIProp::GetProps](imapiprop-getprops.md)でホスト受信者のプロパティ値を前処理および後処理します。
    
- **IMAPIProp::OpenProperty** で、ボタンやリスト ボックスなどの詳細表示テーブル コントロールを処理します。
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)でホスト受信者のプロパティ値を検証または操作します。
    
- ホスト受信者を[IMAPIProp::SaveChanges](imapiprop-savechanges.md)に保存する前に、PR_EMAIL_ADDRESS などの必須プロパティを計算し、必要なすべてのプロパティが設定されているのを確認します。 
    
### <a name="to-implement-iablogonopentemplateid"></a>IABLogon::OpenTemplateID を実装するには
  
1. _lpTemplateID_ パラメーターで渡されたテンプレート識別子が有効で、プロバイダーが認識する形式にあるか確認します。 エラーが発生しない場合は、エラーが発生し、MAPI_E_INVALID_ENTRYID。 
    
2. テンプレート識別子で示される種類のオブジェクト (メッセージング ユーザー、配布リスト、または一時受信者) を作成します。 
    
3. _lpMAPIPropData_ パラメーターが指すオブジェクトであるホスト プロバイダーのプロパティ オブジェクトで **、IUnknown::AddRef** メソッドを呼び出します。 
    
4. _ulTemplateFlags_ パラメーターが次の値に設定FILL_ENTRY。 
    
   1. 新しいオブジェクトがメッセージング ユーザーまたは配布リストの場合:
      
      1. **IMAPIProp::GetProps** メソッドを呼び出して、新しいオブジェクトのすべてのプロパティを取得します。 
          
      2. ホスト プロバイダーの **IMAPIProp::SetProps** メソッドを呼び出して、取得したプロパティをホスト プロバイダーのプロパティ オブジェクトにコピーします。 
      
   2. 新しいオブジェクトが 1 回の受信者である場合は、ホスト プロバイダーの **IMAPIProp::SetProps** メソッドを呼び出して、次のプロパティを設定します。 
      
      - **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)をプロバイダーが処理するアドレスの種類に設定します。
        
      - **PR \_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) を  _lpTemplateID_ パラメーターと  _cbTemplateID_ パラメーターからテンプレート識別子に指定します。 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して、DT_MAILUSERまたはDT_DISTLISTに設定します。
    
5. プロバイダーがラップされたオブジェクトが必要であると判断するかどうかに応じて  _、lppMAPIPropNew_ パラメーターの内容を、プロバイダーの新しいオブジェクトまたは  _lpMAPIPropData_ パラメーターで渡されたプロパティ オブジェクトを指す値を設定します。 
    
6. ネットワーク障害やメモリ切れなどの重大なエラーが発生した場合は、適切なエラー値を返します。 この値は、ホスト プロバイダーによって実行されるタスクである [、適切な MAPIERROR](mapierror.md) 構造を使用してクライアントに伝達される必要があります。 
    

