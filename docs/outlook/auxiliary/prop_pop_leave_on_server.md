---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: POP アカウントのサーバーにメッセージのコピーを残すかを指定します。
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799570"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

POP アカウントのサーバーにメッセージのコピーを残すかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x1000  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ。  <br/> |0x10000003  <br/> |
|アクセス:  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

次の表は、可能な値を一覧します。 定数の詳細については[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。 
  
|**使用可能な値**|**説明**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |デバイスにメッセージをダウンロードした後、POP サーバーにメッセージのコピーを残します。  <br/> |
|**REMOVE_AFTER** <br/> |デバイスにダウンロードした後、POP サーバーからメッセージを削除します。  <br/> |
|**REMOVE_ON_NUKE** <br/> |ユーザーが削除済みアイテム フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |POP サーバーから、メッセージを削除するまでの日数を取得します。  <br/> |
|**SET_REMOVE_AFTER_DAYS**(_日_)  <br/> |POP サーバーから、メッセージを削除するまでの日数を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [管理メッセージは、POP3 アカウントのダウンロードします。](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

