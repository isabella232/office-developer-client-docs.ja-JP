---
title: 会議の更新オプションのプロパティを非表示にする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412101"
---
# <a name="hide-meeting-update-option-property"></a>会議の更新オプションのプロパティを非表示にする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
追加または削除された出席者にのみ会議の更新を送信するオプションを非表示にします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開:  <br/> |[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト  <br/> |
|作成者:  <br/> |ストアプロバイダー  <br/> |
|アクセス先:  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。 これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。 ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。
  
|||
|:-----|:-----|
|lpguid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulkind:  <br/> |MNID_STRING  <br/> |
|種類が lpwstrname:  <br/> |L "urn: スキーマ-microsoft-com: office: outlook # allornonemtgupdatedlg"  <br/> |
   
サーバーを使用して会議の更新を送信するストアプロバイダーは、[**出席者への更新プログラムの送信**] ダイアログボックスを変更することができます。 この機能は、サーバーが会議の更新を送信するときに、最初の会議出席依頼以降にユーザーが追加または削除した出席者がわからないために役立ちます。 このプロパティに**true**が設定されている場合、[**出席者に更新**を送信] ダイアログボックスに [出席者に更新**のみを**送信] オプションが表示されません。 
  
outlook のバージョンが Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。
  

