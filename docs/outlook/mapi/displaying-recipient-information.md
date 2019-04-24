---
title: 受信者情報の表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337038"
---
# <a name="displaying-recipient-information"></a>受信者情報の表示

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI には、受信者の詳細を表示するためのコモンダイアログボックスが用意されています。 [詳細] ダイアログボックスは、表示テーブルと**imapiprop**の実装から作成されます。 表示テーブルは、詳細表示の外観を示し、 **imapiprop**の実装は受信者のデータを制御します。 プロバイダーは、受信者ごとに表示テーブルと**imapiprop**実装を提供する必要があります。 
  
表示テーブルを作成する最も簡単な方法は、 [dtpage](dtpage.md)構造を定義して[builddisplaytable](builddisplaytable.md)を呼び出すことです。 ただし、1回限りの受信者の作成を許可するプロバイダーによっては、特に読み取り専用プロバイダーがある場合は、 **ipropdata**を使用します。 **imapiprop**の実装には、任意の種類の property オブジェクトを指定できます。 
  
このダイアログボックスを呼び出すには、次の2つの方法があります。 [IAddrBook::D etails](iaddrbook-details.md) and [imapisupport::D etails](imapisupport-details.md)。 プロバイダーが、受信者の詳細を要求するために、これらのメソッドのいずれかを呼び出すと、まず、まず、そのコンテナーの[IMAPIContainer:: openentry](imapicontainer-openentry.md)メソッドを呼び出して受信者を開きます。 次に、受信者の[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求します。 **PR_DETAILS_TABLE**は、受信者の詳細表示テーブルを表すプロパティです。 
  
次の手順で説明するように、 [ipropdata: imapiprop](ipropdataimapiprop.md)インターフェイスを使用して、表示テーブルコントロールの変更を監視できます。 
  
## <a name="monitor-changes-to-a-control"></a>コントロールに加えられた変更を監視する
  
1. ユーザーがコントロールにアクセスできるようにするには、 [ipropdata:: HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出して、コントロールのアクセスを IPROP_CLEAN に設定します。 
    
2. ユーザーがダイアログボックスで作業できるようにします。 
    
3. ユーザーが終了したら、 [ipropdata:: hrgetpropaccess](ipropdata-hrgetpropaccess.md)を呼び出して、コントロールの現在のアクセスレベルを取得します。 
    
4. アクセスレベルが IPROP_DIRTY の場合、ユーザーはコントロールを変更しています。 プロバイダーは次のようにする必要があります。
    
   - [ipropdata:: hrsetpropaccess](ipropdata-hrsetpropaccess.md)を呼び出して、アクセスレベルを IPROP_CLEAN に戻します。 
    
   - プロパティデータオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、変更されたプロパティを取得し、 [imapiprop:: setprops](imapiprop-setprops.md)を呼び出して更新します。
    
5. アクセスレベルが依然として IPROP_CLEAN の場合、コントロールは変更されていません。 
    
表示テーブルの作成の詳細については、「[表の表示](display-tables.md)」を参照してください。
  

