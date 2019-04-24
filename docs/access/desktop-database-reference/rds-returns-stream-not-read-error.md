---
title: RDS によって返される「ストリームが読み取れません」のエラー
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300855"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="b2f7b-102">RDS は\"ストリームを読み取る\"ことができませんエラー</span><span class="sxs-lookup"><span data-stu-id="b2f7b-102">RDS returns \"Stream Not Read\" error</span></span>


<span data-ttu-id="b2f7b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2f7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2f7b-p101">"現在の位置がストリームの終わりにあるか、空のためストリーム オブジェクトを読み取れません。空でないストリームについては、現在の位置を Position プロパティで設定してください。ストリームが空かどうかを見るには、Size プロパティを確認してください。"</span><span class="sxs-lookup"><span data-stu-id="b2f7b-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="b2f7b-p102">このエラーが発生した場合、http でパラメーター化された階層クエリを使用しようとしたことが原因である可能性があります。RDS では、パラメーター化された階層をリモートで操作できません。</span><span class="sxs-lookup"><span data-stu-id="b2f7b-p102">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http. RDS does not permit you to remote parameterized hierarchies.</span></span>

