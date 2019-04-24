---
title: PidTagMessageStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355721"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテンツテーブル内のメッセージの状態を定義するフラグの32ビットビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MSG_STATUS  <br/> |
|識別子:  <br/> |0x0e17  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

メッセージは、コンテンツテーブルと1つ以上の検索結果テーブルに存在し、メッセージの各インスタンスの状態が異なる場合があります。 このプロパティは、メッセージのプロパティではなく、contents テーブルの列であるとみなされません。 
  
クライアントアプリケーションでは、このプロパティに次の1つ以上のフラグを設定できます。 
  
MSGSTATUS_ANSWERED 
  
> メッセージに返信しました。 
    
MSGSTATUS_DELMARKED 
  
> このメッセージは、その後の削除のためにマークされています。 
    
MSGSTATUS_DRAFT 
  
> メッセージは下書きの改訂状態です。 
    
MSGSTATUS_HIDDEN 
  
> メッセージは、受信者のフォルダー表示から抑制されます。 
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージは、受信者のフォルダー表示で強調表示されます。 
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージがリモートメッセージストアで削除対象としてマークされ、ローカルクライアントにダウンロードされていません。 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモートメッセージストアからローカルクライアントにダウンロードするようにマークされています。 
    
MSGSTATUS_TAGGED 
  
> メッセージには、クライアント定義の目的のタグが付けられています。
    
**MSGSTATUS_DELMARKED**、 **MSGSTATUS_HIDDEN**、 **MSGSTATUS_HIGHLIGHTED**、および**MSGSTATUS_TAGGED**の各フラグはクライアントによって定義されます。 トランスポートプロバイダーとストアプロバイダーは、操作を行わずにこれらのビットを渡します。 
  
クライアントは、これらの値をアプリケーションに適した方法で解釈できます。 多くのクライアントがこのプロパティを使用する方法の1つは、削除対象としてマークされたメッセージを代表アイコンで表示することです。 
  
リモートビューアークライアントは、リモートトランスポートプロバイダーによって提供されるヘッダーフォルダー内のメッセージに**MSGSTATUS_REMOTE_DELETE**または**MSGSTATUS_REMOTE_DOWNLOAD**を設定できます。 クライアントアプリケーションは、このフォルダー内の各メッセージヘッダーを調べて、リモートメッセージストアでメッセージをダウンロードまたは削除する必要があるかどうかを判断できます。 次に、 [imapifolder:: setmessagestatus](imapifolder-setmessagestatus.md)メソッドを使用して、適切なフラグを設定します。 **setmessagestatus**は、このプロパティの任意のフラグを設定する唯一の方法です。[imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用することはできません。 このプロパティを取得するために、クライアントは imapifolder [:: GetProps](imapiprop-getprops.md)ではなく、 [imapifolder:: getmessagestatus](imapifolder-getmessagestatus.md)を呼び出します。
  
このプロパティのビット16から 31 (の場合は 0x80000000 ~ 0x80000000) は、個人間メッセージ (IPM) クライアントアプリケーションで使用できます。 他のすべてのビットは MAPI での使用のために予約されています。前の表で定義されていないものは、最初は0に設定され、その後は変更されません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

