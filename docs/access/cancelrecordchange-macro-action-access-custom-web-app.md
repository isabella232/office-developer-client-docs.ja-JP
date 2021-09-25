---
title: CancelRecordChange マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: CancelRecordChange/レコードの変更の取り消しアクションを使用して、変更を確定する前に CreateRecord または EditRecord データ ブロック内でレコードに適用した変更を取り消すことができます。
ms.openlocfilehash: 592ff1fae39956c9f1fe638072b5aeda41badb1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573300"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a>CancelRecordChange マクロ アクション (Access カスタム Web アプリ)

You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**CancelRecordChange/レコードの変更の取り消し**" アクションは、データ マクロ内でのみ使用できます。 
  
## <a name="remarks"></a>注釈

"**CancelRecordChange/レコードの変更の取り消し**" アクションを呼び出すと、**CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。 
  

