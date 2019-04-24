---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326125"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 階層アドレスルート (HAB) の識別名 (DN) を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT、PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|プロパティセット:  <br/> |アドレス帳  <br/> |
|ロング ID (LID):  <br/> |0x8c98  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |Exchange アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

これはグローバルアドレス一覧 (GAL) コンテナーのプロパティであり、階層的なアドレスルートの識別名を表します。 このプロパティは、オフラインアドレス帳にのみ存在し、Active Directory ドメインサービス (AD DS) には含まれません。 呼び出し元は、リモートプロシージャコールを回避するために MAPI_CACHE_ONLY を GetProps 呼び出しに渡す必要があります。 このパラメーターが存在しない場合、発信者は PT_OBJECT 型の PR_EMS_AB_HAB_ROOT_DEPARTMENT を使用して、ルート部署を検索する必要があります。 
  
ルート部門が取得されると、MAPI_MAILUSER または MAPI_DISTLIST のオブジェクトタイプを持つことができます。 オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。 オブジェクトの種類が MAPI_MAILUSER の場合、前のスキーマが使用されています。 
  
- Microsoft Office Outlook 2007 Service Pack 2 は、両方のスキーマをサポートしています。 
    
- microsoft outlook 2010 および microsoft outlook 2013 は、新しいスキーマをサポートしています。
    
新しいスキーマでは、すべての部署グループが配布リストであり、MAPI_DISTLIST 型でもあります。 部署グループのメンバー、および部署グループ内の部署は、PR_EMS_AB_MEMBER を使用して配布リストのメンバーとまったく同じように取得されます。
  
ルート部門が取得されると、MAPI_MAILUSER または MAPI_DISTLIST のオブジェクトタイプを持つことができます。 オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。 オブジェクトの種類が MAPI_MAILUSER の場合は、古いスキーマが使用されています。 
  
新しいスキーマでは、すべての部署グループは dl でもあり、MAPI_DISTLIST 型です。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

