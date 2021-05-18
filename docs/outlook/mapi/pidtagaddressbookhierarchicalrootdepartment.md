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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326125"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 階層アドレス ルート (HAB) の識別名 (DN) が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT,PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|プロパティ セット:  <br/> |アドレス帳  <br/> |
|長い ID (LID):  <br/> |0x8C98  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |Exchangeアドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これはグローバル アドレス一覧 (GAL) コンテナーのプロパティであり、階層型アドレス ルートの識別名を表します。 このプロパティはオフライン アドレス帳にのみ存在し、Active Directory ドメイン サービス (DS) にはADされません。 呼び出し元は、MAPI_CACHE_ONLYプロシージャ呼び出しを回避するために、GetProps 呼び出しに渡す必要があります。 これが存在しない場合、発信者はルート部門PR_EMS_AB_HAB_ROOT_DEPARTMENTの種類である PT_OBJECT を使用する必要があります。 
  
ルート部門を取得すると、オブジェクトの種類を指定MAPI_MAILUSERまたはMAPI_DISTLIST。 オブジェクトの種類が変更MAPI_DISTLIST新しいスキーマが採用されています。 オブジェクトの種類が変更MAPI_MAILUSER前のスキーマが使用されています。 
  
- Microsoft Office Outlook 2007 Service Pack 2 では、両方のスキーマがサポートされています。 
    
- Microsoft Outlook 2010とMicrosoft Outlook 2013スキーマをサポートします。
    
新しいスキーマでは、すべての部門グループも配布リストであり、種類は MAPI_DISTLIST。 部署グループのメンバー、および部門グループ内の部署は、配布リスト のメンバーとまったく同PR_EMS_AB_MEMBERを使用して取得されます。
  
ルート部門を取得すると、オブジェクトの種類を指定MAPI_MAILUSERまたはMAPI_DISTLIST。 オブジェクトの種類が指定されているMAPI_DISTLIST、新しいスキーマが使用されています。 オブジェクトの種類が指定されているMAPI_MAILUSER、古いスキーマが使用されています。 
  
新しいスキーマでは、すべての部署グループも LS で、グループの種類MAPI_DISTLIST。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのMicrosoft Exchange Serverを提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

