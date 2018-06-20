---
title: テーブルの終了を決定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799910"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="3be84-103">テーブルの終了を決定します。</span><span class="sxs-lookup"><span data-stu-id="3be84-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="3be84-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3be84-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3be84-105">一般的なエラーでは、こと、テーブルの末尾に達しました場合を想定しています。</span><span class="sxs-lookup"><span data-stu-id="3be84-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="3be84-106">[IMAPITable::QueryRows](imapitable-queryrows.md)は、 [IMAPITable::GetRowCount](imapitable-getrowcount.md)によって返される行の数によって決定されるループの最後に、ループ内で呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="3be84-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="3be84-107">**な**を表すカウント常にはありません。 テーブル内の行の正確な数おおよそのカウントすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3be84-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="3be84-108">**QueryRows**が固定数の行で呼び出されより少ない行が返されます。</span><span class="sxs-lookup"><span data-stu-id="3be84-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="3be84-109">**QueryRows**がそれ以上の行を取得するのにはゼロに等しい行の数を設定する行を返すまでではなくをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3be84-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="3be84-110">呼び出し元が正行の数については、表の最後に、または負の値の行の数については、表の先頭にカーソルが配置されていることを引き受けることが唯一の時間は、値 S_OK は、0 個の行が返されたときです。</span><span class="sxs-lookup"><span data-stu-id="3be84-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="3be84-111">値 MAPI_E_NOT_FOUND が返されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3be84-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3be84-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3be84-112">See also</span></span>



[<span data-ttu-id="3be84-113">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="3be84-113">MAPI Tables</span></span>](mapi-tables.md)

