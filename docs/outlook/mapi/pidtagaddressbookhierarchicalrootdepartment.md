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
ms.openlocfilehash: 49c9b0a80f9bc3b45dfafa6f4e037fe55af289d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802483"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**適用対象**: Outlook 
  
 (HAB) の階層構造のアドレスのルートの識別名 (DN) が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT、PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|プロパティを設定します。  <br/> |アドレス帳  <br/> |
|長い ID (LID):  <br/> |0x8C98  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|領域:  <br/> |Exchange アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これは、グローバル アドレス一覧 (GAL) コンテナーのプロパティであり、階層的なアドレスのルートの識別名を表します。 このプロパティは、Active Directory ドメイン サービス (AD DS) しないとオフライン アドレス帳に存在だけです。 呼び出し元は、リモート プロシージャ呼び出しを避けるために GetProps 呼び出しに MAPI_CACHE_ONLY を渡す必要があります。 これが存在しない場合、呼び出し元は、ルート部署が見つかりません PT_OBJECT の種類は、PR_EMS_AB_HAB_ROOT_DEPARTMENT を使用する必要があります。 
  
ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。 オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマを採用します。 オブジェクトの種類が MAPI_MAILUSER の場合は、前のスキーマを採用されています。 
  
- Microsoft Office Outlook 2007 Service Pack 2 には、両方のスキーマがサポートされています。 
    
- Microsoft Outlook 2010 および Microsoft Outlook 2013 は、新しいスキーマをサポートします。
    
新しいスキーマで部門のすべてのグループも、配布リスト、MAPI_DISTLIST の種類の。 部門のグループ、および部門別のグループ内の部門のメンバーを取得するには、配布リストのメンバーと同様に PR_EMS_AB_MEMBER を使用します。
  
ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。 オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。 オブジェクトの種類が MAPI_MAILUSER の場合は、古いスキーマが使用されています。 
  
新しいスキーマですべての部門別のグループも Dl、型 MAPI_DISTLIST の。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

