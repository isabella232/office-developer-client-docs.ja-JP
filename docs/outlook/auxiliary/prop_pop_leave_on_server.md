---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: POP アカウントのサーバーにメッセージのコピーを残す方法を指定します。
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410946"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

POP アカウントのサーバーにメッセージのコピーを残す方法を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x1000  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ:  <br/> |0x10000003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

次の表に、使用可能な値を示します。 定数 [の詳細については、「定数 (アカウント管理 API)」](constants-account-management-api.md) を参照してください。 
  
|**可能な値**|**説明**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |デバイスにメッセージをダウンロードした後、POP サーバーにメッセージのコピーを残します。  <br/> |
|**REMOVE_AFTER** <br/> |デバイスにダウンロードした後、POP サーバーからメッセージを削除します。  <br/> |
|**REMOVE_ON_NUKE** <br/> |ユーザーが削除済みアイテム フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |メッセージが POP サーバーから削除される日数を取得します。  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _日_)  <br/> |メッセージが POP サーバーから削除される日数を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

