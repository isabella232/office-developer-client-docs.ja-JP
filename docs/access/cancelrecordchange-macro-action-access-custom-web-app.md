---
title: cancelrecordchange マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: CancelRecordChange/レコードの変更の取り消しアクションを使用して、変更を確定する前に CreateRecord または EditRecord データ ブロック内でレコードに適用した変更を取り消すことができます。
ms.openlocfilehash: fe95718e752513c4b8b700f331fec7b78092e553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280761"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a>cancelrecordchange マクロアクション (Access カスタム web アプリ)

You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed. 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**CancelRecordChange/レコードの変更の取り消し**" アクションは、データ マクロ内でのみ使用できます。 
  
## <a name="remarks"></a>解説

"**CancelRecordChange/レコードの変更の取り消し**" アクションを呼び出すと、**CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。 
  

