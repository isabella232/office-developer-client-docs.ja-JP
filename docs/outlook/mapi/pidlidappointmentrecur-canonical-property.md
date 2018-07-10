---
title: PidLidAppointmentRecur の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801766"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>PidLidAppointmentRecur の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で指定されている範囲、定期的なパターンのいずれかを使用して定期的な系列が発生したときの日付と時刻を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidApptRecur  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008216  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、一連の定期的な定期的なパターンのいずれかで発生して範囲の詳細な[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)日付と時刻を指定します。 このプロパティの値は、変更と削除の両方の例外に関する情報も含まれています。日付、件名、場所、およびその他のいくつかの例外のプロパティなどの情報。 定期的な予定表アイテムのこのプロパティのバイナリ データは、 **AppointmentRecurrencePattern**構造体として格納されます。 このプロパティは、単一インスタンスの予定表アイテムに存在する必要があります。 
  
定期的なアイテムをいくつかの制限があります。
  
- 複数のインスタンスは、同じ日に開始する必要がありますできません。
    
- 出現回数が重複する必要があります。 具体的には、以前のインスタンスの末尾と次の定期的な系列のインスタンスの開始後の日付に定期的な系列のインスタンスの開始日を変更するの例外が発生する必要があります。 定期的な系列の前または次のインスタンスが例外の場合も同様です。
    
一連の定期的なスケジュールは、その定期的なパターンと範囲が決定されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
