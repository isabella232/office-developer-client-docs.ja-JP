---
title: 受信者情報を表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7071c05f6f59740163f97f840c7fa48d83bea815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799952"
---
# <a name="displaying-recipient-information"></a>受信者情報を表示します。

**適用されます**: Outlook 
  
MAPI には、受信者の詳細を表示するためのコモン ダイアログ ボックスが用意されています。 **IMAPIProp**実装とディスプレイ テーブルから、[詳細情報] ダイアログ ボックスが作成されます。 表示された表の詳細の表示の外観を記述して、 **IMAPIProp**の実装は、受信者のデータを制御します。 プロバイダーは、表示された表と各受信者の**IMAPIProp**の実装を提供する必要があります。 
  
[DTPAGE](dtpage.md)構造体を定義し、 [BuildDisplayTable](builddisplaytable.md)を呼び出すには、表示された表を作成する最も簡単な方法です。 ただし、一部のプロバイダーでは、具体的には読み取り専用プロバイダーを 1 回限りの受信者の作成は、 **IPropData**を使用します。 **IMAPIProp**の実装は、オブジェクトのプロパティの任意の型にできます。 
  
このダイアログ ボックスを起動するための 2 つの方法があります: [IAddrBook::Details](iaddrbook-details.md)と[IMAPISupport::Details](imapisupport-details.md)。 プロバイダーを呼び出すと、受信者の詳細を要求するこれらのメソッドのいずれか、MAPI はまずコンテナーの[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを呼び出すことによって、受信者を開きます。 次に**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するための受信者の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 **PR_DETAILS_TABLE**は、受信者の詳細表示のテーブルを表すプロパティです。 
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)以下の手順で説明したようにテーブル コントロールの表示上の変更を監視するインターフェイスを使用することができます。 
  
## <a name="monitor-changes-to-a-control"></a>コントロールへの変更を監視します。
  
1. ユーザーは、コントロールへのアクセス権を取得、前に、コントロールのアクセスを IPROP_CLEAN に設定するのには[IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出します。 
    
2. ダイアログ ボックスを操作するユーザーを許可します。 
    
3. ユーザーが完了したら、コントロールの現在のアクセス レベルを取得するために[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)を呼び出します。 
    
4. アクセス レベルが IPROP_DIRTY の場合は、ユーザーがコントロールを変更します。 プロバイダーは次のとおりです。
    
   - IPROP_CLEAN にレベルのアクセス権を設定するのには[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)を呼び出します。 
    
   - プロパティの変更を取得し、 [IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出すことによって更新するのには、プロパティのデータ オブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。
    
5. アクセス レベルがまだ IPROP_CLEAN である場合、コントロールは変更されていません。 
    
表示のテーブルを作成する方法の詳細については、[テーブルの表示](display-tables.md)を参照してください。
  

