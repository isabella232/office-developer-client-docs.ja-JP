---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348854"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルの管理をサポートします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|公開者:  <br/> |プロファイル管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IProfAdmin  <br/> |
|ポインターの種類:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |プロファイル管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[getprofiletable](iprofadmin-getprofiletable.md) <br/> |利用可能なすべてのプロファイルについての情報を含むテーブルである、プロファイルテーブルへのアクセスを提供します。  <br/> |
|[createprofile](iprofadmin-createprofile.md) <br/> |新しいプロファイルを作成します。  <br/> |
|[deleteprofile](iprofadmin-deleteprofile.md) <br/> |プロファイルを削除します。  <br/> |
|[changeprofilepassword](iprofadmin-changeprofilepassword.md) <br/> |現在は廃止されています。 プロファイルのパスワードを変更します。  <br/> |
|[copyprofile](iprofadmin-copyprofile.md) <br/> |プロファイルをコピーします。  <br/> |
|[renameprofile](iprofadmin-renameprofile.md) <br/> |プロファイルに新しい名前を割り当てます。  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |クライアントの既定のプロファイルを設定またはクリアします。  <br/> |
|[adminservices](iprofadmin-adminservices.md) <br/> |プロファイル内のメッセージサービスに変更を加えるためのメッセージサービス管理オブジェクトへのアクセスを提供します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

