---
title: PidTagReceivedRepresentingAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 14c501c0d0fc83903dc65a69647e382a775c2edf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599671"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a>PidTagReceivedRepresentingAddressType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを実際に受信したユーザーによって表されるメッセージング ユーザーのアドレスの種類を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RCVD_REPRESENTING_ADDRTYPE、PR_RCVD_REPRESENTING_ADDRTYPE_A、PR_RCVD_REPRESENTING_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x0077  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、受信ユーザーによって表されるメッセージング ユーザーのアドレス プロパティの例です。 これは、代理人の承認または検証を担当する受信トランスポート プロバイダーによって設定する必要があります。 メッセージング ユーザーが表されていない場合、このプロパティは **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) プロパティに含まれるアドレスの種類に設定する必要があります。
  
別のクライアントに代わって受信したメッセージに返信するクライアント アプリケーションは、このプロパティを受信したメッセージから返信の **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType)](pidtagsentrepresentingaddresstype-canonical-property.md)プロパティにコピーする必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagAddressType 標準プロパティ](pidtagaddresstype-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

