---
title: Update 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: 指定したフィールドに対して INSERT 操作または UPDATE 操作が試行されたかどうかを返します。
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410918"
---
# <a name="update-function-access-custom-web-app"></a>Update 関数 (Access カスタム Web アプリ)

指定したフィールドに対して INSERT 操作または UPDATE 操作が試行されたかどうかを返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **更新** (*列*) 
  
**Update 関数には**、次の引数が含まれます。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Column*  <br/> |INSERT 操作または UPDATE 操作をチェックするフィールドの名前。  <br/> |
   
## <a name="remarks"></a>注釈

**Update 関数** は、INSERT または UPDATE の試行が成功したかどうかに関係なく、TRUE を返します。 
  

