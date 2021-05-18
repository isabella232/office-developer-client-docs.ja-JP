---
title: プロパティ識別子の範囲
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422706"
---
# <a name="property-identifier-ranges"></a>プロパティ識別子の範囲

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の表は、各範囲のプロパティの所有者を示す、プロパティ識別子の異なる範囲の概要を示しています。
  
|**識別子の範囲**|**説明**|
|:-----|:-----|
|0000  <br/> |特別な値を使用して MAPI によって **予約** PR_NULL。  <br/> |
|0001 - 0BFF  <br/> |MAPI で定義されたメッセージ エンベロープ プロパティ。  <br/> |
|0C00 - 0DFF  <br/> |MAPI によって定義された受信者プロパティ。  <br/> |
|0E00 - 0FFF  <br/> |MAPI によって定義された送信不可のメッセージ プロパティ。  <br/> |
|1000 - 2FFF  <br/> |MAPI によって定義されたメッセージ コンテンツ プロパティ。  <br/> |
|3000 - 3FFF  <br/> |MAPI によって定義されたメッセージおよび受信者以外のオブジェクトのプロパティ。  <br/> |
|4000 ~ 57FF  <br/> |トランスポート プロバイダーによって定義されるメッセージ エンベロープ プロパティ。  <br/> |
|5800 - 5FFF  <br/> |トランスポート プロバイダーとアドレス帳プロバイダーによって定義される受信者プロパティ。  <br/> |
|6000 ~ 65FF  <br/> |クライアントによって定義された送信不可のメッセージ プロパティ。  <br/> |
|6600 - 67FF  <br/> |サービス プロバイダーによって定義された送信不可のプロパティ。 これらのプロパティは、ユーザーに表示または非表示にすることができます。  <br/> |
|6800 - 7BFF  <br/> |これらのクラスの作成者によって定義されたカスタム メッセージ クラスのメッセージ コンテンツ プロパティ。  <br/> |
|7C00 - 7FFF  <br/> |これらのクラスの作成者によって定義されたカスタム メッセージ クラスの送信不可プロパティ。  <br/> |
|8000 - FFFE  <br/> |[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)および[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用して名前で識別されるクライアントおよび場合によってはサービス プロバイダーによって定義されるプロパティ。  <br/> |
|FFFF  <br/> |特別なエラー値を使用して MAPI によって予約PROP_ID_INVALID。  <br/> |
   
3000 ~ 3FFF の範囲は、メッセージまたは受信者に関連しないプロパティ用に予約されています。 MAPI は、この範囲をオブジェクトの種類によってサブ範囲に分割します。次の表に、この詳細な内訳を示します。 
  
|**識別子の範囲**|**プロパティの種類**|
|:-----|:-----|
|3000 ~ 33FF  <br/> |複数のオブジェクトに表示される一般的なプロパティ (PR_DISPLAY_NAME、PR_ENTRYID)。    <br/> |
|3400 ~ 35FF  <br/> |メッセージ ストアのプロパティ  <br/> |
|3600 ~ 36FF  <br/> |フォルダーとアドレス帳コンテナーのプロパティ  <br/> |
|3700 - 38FF  <br/> |添付ファイルのプロパティ  <br/> |
|3900 - 39FF  <br/> |アドレス帳のプロパティ  <br/> |
|3A00 - 3BFF  <br/> |メッセージング ユーザーのプロパティ  <br/> |
|3C00 - 3CFF  <br/> |配布リストのプロパティ  <br/> |
|3D00 - 3DFF  <br/> |プロファイル プロパティ  <br/> |
|3E00 - 3FFF  <br/> |Status オブジェクトのプロパティ  <br/> |
   

