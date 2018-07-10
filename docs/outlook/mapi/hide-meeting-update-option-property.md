---
title: 会議の更新のオプションのプロパティを非表示にします。
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800207"
---
# <a name="hide-meeting-update-option-property"></a>会議の更新のオプションのプロパティを非表示にします。

  
  
**適用されます**: Outlook 
  
のみ追加または削除された出席者に会議の更新を送信するオプションを非表示にします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開されます。  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト  <br/> |
|によって作成されます。  <br/> |ストア プロバイダー  <br/> |
|によってアクセスします。  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。 これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。 ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。 
  
このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind。  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName。  <br/> |L"urn: スキーマ-マイクロソフト-com:office:outlook #allornonemtgupdatedlg」  <br/> |
   
ストア プロバイダー、サーバーを使用して、会議の更新を送信するには、**出席者に更新内容を送信**] ダイアログ ボックスで変更できます。 どの参加者が追加されたり、最初の会議出席依頼した後にユーザーが削除サーバーでは、会議の更新を送信するとき、サーバーは認識できないために、この機能の使用をお勧めします。 このプロパティが**true**の場合、**出席者に更新を送信**] ダイアログ ボックスで**追加または削除された出席者にのみ更新を送信**する] オプションは表示されません。 
  
Outlook のバージョンの Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。
  
