---
title: PidLidAppointmentTimeZoneDefinitionStartDisplay の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801826"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionStartDisplay の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
単独の予定または会議出席依頼の開始時刻を選択するために使用されるタイム ゾーンの説明を格納する[TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidApptTZDefStartDisplay  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000825E  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>備考

2003 または以前のバージョンを Microsoft Office Outlook とソリューションにコラボレーション データ オブジェクト (CDO) 1.2.1 を置くし、Outlook または Microsoft Exchange Server では、予定表更新ツールを実行していないことは、シングル ・ インスタンスの終了時刻と開始時刻を格納します。予定および会議出席依頼で世界協定時刻 (UTC)。 これらのクライアントは、予定または会議出席依頼が作成されるタイム ゾーンの情報を格納していません。
  
、Microsoft Office Outlook 2007 と Outlook または Exchange Server の予定表更新ツールを実行している CDO 1.2.1 ベースのソリューションは、このプロパティを使用して、開始時刻のタイム ゾーンを格納するための Outlook のバージョン。 **DispidApptTZDefStartDisplay**プロパティは、元のタイム ゾーンでの予定または会議を示していますが予定されているを提供。 タイム ゾーンの規則を変更する場合に、開始時刻を調整する必要があるかどうかを決定します。 このプロパティが存在しない場合は、現在のローカル タイム ゾーンと見なされます。 このプロパティは、表示目的でのみ使用されるが、定期的なアイテムの展開で使用されていません。 
  
パーサーは、 **dispidApptTZDefStartDisplay**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合や、このプロパティから取得したストリームを読み取るとき注意が必要である必要があります。 詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。
  
このプロパティは、 **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) のプロパティのタイム ゾーン情報を指定します。 UTC からの開始日と時刻を表示のためのローカル タイム ゾーンに変換するのには、 **dispidApptTZDefStartDisplay**の値が使用されます。 各**TZRULE**このプロパティで指定された、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定しないでください。 たとえば、 **TZRULE**が有効なルールの場合は、 **TZRULE**フィールドの値必要があります「0x0002」です。それ以外の場合、"0x0000"である必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照が用意されています。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

