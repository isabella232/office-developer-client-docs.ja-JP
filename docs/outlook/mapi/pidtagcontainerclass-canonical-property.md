---
title: PidTagContainerClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9d40c21cde6bf3a6e8e37dda80dd6f900f233a0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802590"
---
# <a name="pidtagcontainerclass-canonical-property"></a>PidTagContainerClass の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーの種類を説明する文字列が含まれています。 このプロパティを無視することが一般的には、Exchange Server 2003 のメールボックス マネージャーの前に、Microsoft® Exchange Server のバージョンはこのプロパティが存在することを期待しています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W  <br/> |
|識別子:  <br/> |0x3613  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、通常は Exchange Server では使用されません。 ただし、Microsoft Office Outlook® に添付のメールボックス フォルダーです。 さらに、Exchange Server 2003 のメールボックス マネージャーの前に Exchange Server のバージョンが正しく処理されないこれらのプロパティを持たないフォルダーです。
  
これらのプロパティは、次の表に文字列値を指定できます。
  
|**値**|**フォルダーの内容**|
|:-----|:-----|
|IPF.Appointment  <br/> |予定  <br/> |
|IPF.Contact  <br/> |連絡先  <br/> |
|IPF。仕訳帳  <br/> |Outlook の仕訳帳のエントリ  <br/> |
|IPF.Note  <br/> |メール メッセージおよびノート  <br/> |
|IPF。StickyNote  <br/> |Outlook のメモ  <br/> |
|IPF.Task  <br/> |Outlook のタスク  <br/> |
   
メール メッセージが含まれるフォルダーでは、IPF にこれらのプロパティを設定する必要があります。注意してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

