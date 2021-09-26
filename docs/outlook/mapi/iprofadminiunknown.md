---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a6387de14e7b4ee513168ddd65383c39481c8699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620577"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルの管理をサポートします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|次のユーザーによって公開されます。  <br/> |プロファイル管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IProfAdmin  <br/> |
|ポインターの種類:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |プロファイル管理オブジェクト [に発生](mapierror.md) した以前のエラーに関する情報を含む MAPIERROR 構造体を返します。  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |使用可能なすべてのプロファイルに関する情報を含むテーブルであるプロファイル テーブルへのアクセスを提供します。  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |新しいプロファイルを作成します。  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |プロファイルを削除します。  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |非推奨。 プロファイルのパスワードを変更します。  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |プロファイルをコピーします。  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |プロファイルに新しい名前を割り当てる。  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |クライアントの既定のプロファイルを設定またはクリアします。  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |プロファイル内のメッセージ サービスに変更を加えるメッセージ サービス管理オブジェクトへのアクセスを提供します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

