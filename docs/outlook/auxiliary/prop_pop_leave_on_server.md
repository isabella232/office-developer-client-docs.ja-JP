---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: POP アカウントのサーバーにメッセージのコピーを残すことを指定します。
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326489"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

POP アカウントのサーバーにメッセージのコピーを残すことを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x1000  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティタグ:  <br/> |0x10000003  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

次の表に、使用可能な値を示します。 定数の詳細については、「 [constants (Account management API)](constants-account-management-api.md) 」を参照してください。 
  
|**可能な値**|**説明**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |メッセージをデバイスにダウンロードした後、メッセージのコピーを POP サーバーに残します。  <br/> |
|**REMOVE_AFTER** <br/> |メッセージをデバイスにダウンロードした後、POP サーバーから削除します。  <br/> |
|**REMOVE_ON_NUKE** <br/> |ユーザーが [削除済みアイテム] フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |メッセージが POP サーバーから削除されるまでの日数を取得します。  <br/> |
|**SET_REMOVE_AFTER_DAYS**(_日数_)  <br/> |メッセージが POP サーバーから削除されるまでの日数を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

