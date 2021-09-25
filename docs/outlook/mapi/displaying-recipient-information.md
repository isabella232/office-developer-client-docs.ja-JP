---
title: 受信者情報の表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9318d375341cf1ed8004b7e2043ffd0ce992b678
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596599"
---
# <a name="displaying-recipient-information"></a>受信者情報の表示

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI には、受信者の詳細を表示する一般的なダイアログ ボックスが表示されます。 詳細ダイアログ ボックスは、表示テーブルと **IMAPIProp 実装から作成** されます。 表示テーブルは詳細表示の外観を示し **、IMAPIProp 実装** は受信者のデータを制御します。 プロバイダーは、各受信者に対して表示テーブルと **IMAPIProp 実装** を提供する責任があります。 
  
表示テーブルを作成する最も簡単な方法は [、DTPAGE](dtpage.md) 構造を定義し [、BuildDisplayTable を呼び出す方法です](builddisplaytable.md)。 ただし、一部のプロバイダー、特に 1 回限り受信者の作成を許可する読み取り専用 **プロバイダーでは、IPropData を使用します**。 **IMAPIProp の実装** には、任意の種類のプロパティ オブジェクトを指定できます。 
  
このダイアログ ボックスを呼び出す方法は [、IAddrBook::D etails](iaddrbook-details.md) と [IMAPISupport::D です](imapisupport-details.md)。 プロバイダーが次のいずれかのメソッドを呼び出して受信者の詳細を要求すると、MAPI は最初にコンテナーの [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) メソッドを呼び出して受信者を開きます。 次に、受信者の [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して、PR_DETAILS_TABLE **(** [PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求します。 **PR_DETAILS_TABLE** は、受信者の詳細表示テーブルを表すプロパティです。 
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)インターフェイスは、次の手順で説明するように、表示テーブル コントロールの変更を監視するために使用できます。 
  
## <a name="monitor-changes-to-a-control"></a>コントロールへの変更を監視する
  
1. ユーザーがコントロールにアクセスする前に [、IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) を呼び出して、コントロールのアクセス権をコントロールに設定IPROP_CLEAN。 
    
2. ユーザーがダイアログ ボックスを操作できます。 
    
3. ユーザーが終了したら [、IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) を呼び出して、コントロールの現在のアクセス レベルを取得します。 
    
4. アクセス レベルが変更IPROP_DIRTY、ユーザーはコントロールを変更しました。 プロバイダーは以下を行う必要があります。
    
   - [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)を呼び出して、アクセス レベルをユーザーに設定IPROP_CLEAN。 
    
   - プロパティ データ オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、変更されたプロパティを取得し [、IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して更新します。
    
5. アクセス レベルが引き続きIPROP_CLEAN、コントロールは変更されません。 
    
表示テーブルの作成の詳細については、「表示テーブル」 [を参照してください](display-tables.md)。
  

