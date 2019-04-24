---
title: ストアのハッシュ番号を計算するアルゴリズム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 489e0d74-8ecd-23ba-c874-18fd8c50fd12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 12797c2ed96ba2db493b5cf425423ffe97fc7a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331585"
---
# <a name="algorithm-to-calculate-the-store-hash-number"></a><span data-ttu-id="8fe1f-103">ストアのハッシュ番号を計算するアルゴリズム</span><span class="sxs-lookup"><span data-stu-id="8fe1f-103">Algorithm to Calculate the Store Hash Number</span></span>
 
<span data-ttu-id="8fe1f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fe1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fe1f-105">mapi の Uniform resource Locator (URL) の一部として、ストアプロバイダーは、インデックス作成の準備ができているオブジェクトを識別するために、ストアのハッシュ番号を mapi プロトコルハンドラーに送信します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-105">As part of a MAPI Uniform Resource Locator (URL), a store provider sends a store hash number to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="8fe1f-106">MAPI プロトコルハンドラーは、ストアを識別するために、このストアハッシュ番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-106">The MAPI Protocol Handler uses this store hash number to identify a store.</span></span> <span data-ttu-id="8fe1f-107">一般に、ストアプロバイダーは、ストアのマッピング署名に基づいて、store ハッシュ番号を計算します。このプロパティは、ストアの [グローバルプロファイル] セクションで定義されている**[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** プロパティです。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-107">In general, a store provider calculates the store hash number based on the store mapping signature, if the store has the **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** property defined in the global profile section.</span></span> <span data-ttu-id="8fe1f-108">それ以外の場合、ストアプロバイダーはストアエントリ ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-108">Otherwise, the store provider uses the store entry ID.</span></span> <span data-ttu-id="8fe1f-109">ストアのハッシュ値を計算するアルゴリズムでは、あいまいさを識別するストアを最小限に抑える必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-109">The algorithm to calculate the store hash number must minimize ambiguities identifying stores.</span></span> 
  
<span data-ttu-id="8fe1f-110">このトピックでは、Microsoft Office Outlook がストアのマッピングシグネチャまたはエントリ ID とストアファイル名に基づいてストアハッシュ番号を計算するために使用するアルゴリズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-110">This topic describes an algorithm that Microsoft Office Outlook uses to calculate a store hash number based on the store mapping signature or entry ID and the store file name.</span></span> 
  
<span data-ttu-id="8fe1f-111">エンコードされるバイナリ blob は、ほとんどの場合ストアの PR_ENTRYID ですが、キャッシュされた Exchange ストア (パブリックとプライベートの両方) については、バイナリ blob がプロファイルにある PR_MAPPING_SIGNATURE である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-111">The binary blob to be encoded is the PR_ENTRYID of the store in most cases, but for cached Exchange stores, both public and private, the binary blob should be the PR_MAPPING_SIGNATURE, found in the profile.</span></span>
  
<span data-ttu-id="8fe1f-112">パブリックフォルダーストアのバイナリ blob のハッシュを計算した後、OST パスでハッシュ処理を行う前に、"" という文字列を表す定数0x2e505542。PUB "は、一意であることを保証するためににハッシュされます。これは、プライベートストアのハッシュとは区別されます。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-112">After computing the hash for a public folder store's binary blob, but before hashing-in the OST path, the constant 0x2E505542, which represents the string ".PUB", is hashed in to assure it is unique, that is, distinct from the private store's hash.</span></span>
  
<span data-ttu-id="8fe1f-113">サポートコードを使用してプロファイルの関連ビットを調べることができます。これは、ストアがパブリックまたはプライベートであるかどうか、キャッシュされているかどうか、および OST へのパスを特定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-113">The support code culls the relevant bits from the profile, which can be used to determine whether a store is public or private, if it's cached, and the path to the OST.</span></span> <span data-ttu-id="8fe1f-114">このコードをプロジェクトに組み込むには、関数 computestorehash を呼び出します。このハッシュは、セッションポインターと pr\_ENTRYID、pr\_SERVICE_UID、およびメッセージストアテーブル\_から pr MDB_PROVIDER を入力として取得します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-114">To incorporate this code in a project, call the function ComputeStoreHash, which takes as its input the session pointer as well as PR\_ENTRYID, PR\_SERVICE_UID, and PR\_MDB_PROVIDER from the message store table.</span></span> <span data-ttu-id="8fe1f-115">必要な残りの情報はプロファイルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-115">The rest of the information it needs it gets from the profile.</span></span> <span data-ttu-id="8fe1f-116">出力の場合、この関数は、ストアがキャッシュさ\_れた Exchange ストアである場合は pr MAPPING_SIGNATURE から計算されたもの、\_または pr ENTRYID から計算されたハッシュを返します。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-116">For output, this function returns the hash as computed from PR\_MAPPING_SIGNATURE if the store is a cached Exchange store, or the hash as computed from PR\_ENTRYID.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8fe1f-117">HrEmsmdbUIDFromStore サポート機能は、pbGlobalProfileSectionGuid を使用して exchange メールボックスのプロファイルセクションを開く場合の、[複数の exchange アカウント](using-multiple-exchange-accounts.md)に対応した代替の方法です。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-117">The HrEmsmdbUIDFromStore support function is a [Multiple Exchange Accounts](using-multiple-exchange-accounts.md)-aware replacement for using pbGlobalProfileSectionGuid to open the profile section for an Exchange mailbox.</span></span> 
  
```cpp
#define PR_PROFILE_OFFLINE_STORE_PATH_A PROP_TAG(PT_STRING8, 0x6610)
#define PR_PROFILE_OFFLINE_STORE_PATH_W PROP_TAG(PT_UNICODE, 0x6610)
#define CONFIG_OST_CACHE_PRIVATE  ((ULONG)0x00000180)
#define CONFIG_OST_CACHE_PUBLIC   ((ULONG)0x00000400)
HRESULT HrEmsmdbUIDFromStore(IMAPISession* pmsess,
                             MAPIUID* puidService,
                             MAPIUID* pEmsmdbUID)
{
  if (!puidService) return MAPI_E_INVALID_PARAMETER;
  HRESULT hRes = S_OK;
  SRestriction mres = {0};
  SPropValue mval = {0};
  SRowSet* pRows = NULL;
  SRow* pRow = NULL;
  LPSERVICEADMIN spSvcAdmin = NULL;
  LPMAPITABLE spmtab = NULL;
  enum { eEntryID = 0, eSectionUid, eMax };
  static const SizedSPropTagArray(eMax, tagaCols) =
  {
    eMax,
    {
      PR_ENTRYID,
      PR_EMSMDB_SECTION_UID,
    }
  };
  hRes = pmsess->AdminServices(0, (LPSERVICEADMIN*)&spSvcAdmin);
  if (SUCCEEDED(hRes) && spSvcAdmin)
  {
    hRes = spSvcAdmin->GetMsgServiceTable(0, &spmtab);
    if (spmtab)
    {
      hRes = spmtab->SetColumns((LPSPropTagArray)&tagaCols, TBL_BATCH);
      mres.rt = RES_PROPERTY;
      mres.res.resProperty.relop = RELOP_EQ;
      mres.res.resProperty.ulPropTag = PR_SERVICE_UID;
      mres.res.resProperty.lpProp = &mval;
      mval.ulPropTag = PR_SERVICE_UID;
      mval.Value.bin.cb = sizeof(*puidService);
      mval.Value.bin.lpb = (LPBYTE)puidService;
      (void) spmtab->Restrict(&mres, 0);
      (void) spmtab->QueryRows(10, 0, &pRows);
      if (SUCCEEDED(hRes) && pRows && pRows->cRows)
      {
        pRow = &pRows->aRow[0];
        if (pEmsmdbUID && pRow)
        {
          if (PR_EMSMDB_SECTION_UID == pRow->lpProps[eSectionUid].ulPropTag &&
            pRow->lpProps[eSectionUid].Value.bin.cb == sizeof(*pEmsmdbUID))
          {
            memcpy(pEmsmdbUID, pRow->lpProps[eSectionUid].Value.bin.lpb, sizeof(*pEmsmdbUID));
          }
        }
      }
      FreeProws(pRows);
    }
    if (spmtab) spmtab->Release();
  }
  if (spSvcAdmin) spSvcAdmin->Release();
  return hRes;
} // HrEmsmdbUIDFromStore
bool FExchangePrivateStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPrimaryUserGuid);
} // FExchangePrivateStore
bool FExchangePublicStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPublicGuid);
} // FExchangePublicStore
DWORD ComputeHash(ULONG cbStoreEID, LPBYTE pbStoreEID, LPCSTR pszFileName, LPCWSTR pwzFileName, BOOL bPublicStore)
{
  DWORD  dwHash = 0;
  ULONG  cdw    = 0;
  DWORD* pdw    = NULL;
  ULONG  cb     = 0;
  BYTE*  pb     = NULL;
  ULONG  i      = 0;
  if (!cbStoreEID || !pbStoreEID) return dwHash;
  // Shouldn't see both of these at the same time.
  if (pszFileName && pwzFileName) return dwHash;
  // Get the Store Entry ID
  // pbStoreEID is a pointer to the Entry ID.
  // cbStoreEID is the size in bytes of the Entry ID.
  pdw = (DWORD*)pbStoreEID;
  cdw = cbStoreEID / sizeof(DWORD);
  for (i = 0; i < cdw; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pdw++;
  }
  pb = (BYTE *)pdw;
  cb = cbStoreEID % sizeof(DWORD);
  for (i = 0; i < cb; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pb++;
  }
  if (bPublicStore)
  {
    // Augment to assure it is unique, else could be same as private store.
    dwHash = (dwHash << 5) + dwHash + 0x2E505542; // this is '.PUB'
  }
  // To also include the store file name in the hash calculation,
  // pszFileName and pwzFileName are NULL terminated strings with the path and filename of the store.
  if (pwzFileName)
  {
    while (*pwzFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pwzFileName++;
    }
  }
  else if (pszFileName)
  {
    while (*pszFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pszFileName++;
    }
  }
  // dwHash now contains the hash to be used. It should be written in hex when building a URL.
  return dwHash;
} // ComputeHash
void ComputeStoreHash(LPMAPISESSION lpMAPISession, LPSBinary lpEntryID, LPSBinary lpServiceUID, LPSBinary lpProviderUID, DWORD* lpdwSigHash, DWORD* lpdwEIDHash)
{
  HRESULT hRes = S_OK;
  MAPIUID emsmdbUID = {0};
  LPPROFSECT lpProfSect = NULL;
  BOOL fPublicExchangeStore  = FExchangePublicStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fPrivateExchangeStore = FExchangePrivateStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fCached = false;
  LPSPropValue lpConfigProp = NULL;
  LPSPropValue lpPathPropA = NULL;
  LPSPropValue lpPathPropW = NULL;
  LPSPropValue lpMappingSig = NULL;
  LPSTR szPath = NULL; // Do not free.
  LPWSTR wzPath = NULL; // Do not free.
  // Get profile section.
  if (lpServiceUID)
  {
    hRes = HrEmsmdbUIDFromStore(lpMAPISession,
      (LPMAPIUID) lpServiceUID->lpb,
      &emsmdbUID);
    if (SUCCEEDED(hRes))
    {
      hRes = lpMAPISession->OpenProfileSection(&emsmdbUID, NULL, 0, &lpProfSect);
    }
  }
  if (!lpServiceUID || FAILED(hRes))
  {
    // For Outlook 2003/2007, HrEmsmdbUIDFromStore may not succeed,
    // so use pbGlobalProfileSectionGuid instead.
    hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpProfSect);
  }
  if (lpProfSect)
  {
    hRes = HrGetOneProp(lpProfSect, PR_PROFILE_CONFIG_FLAGS, &lpConfigProp);
    if (SUCCEEDED(hRes) && PROP_TYPE(lpConfigProp->ulPropTag) != PT_ERROR)
    {
      if (fPrivateExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PRIVATE) != 0);
      }
      if (fPublicExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PUBLIC) == CONFIG_OST_CACHE_PUBLIC);
      }
    }
    if (fCached)
    {
      hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_W, &lpPathPropW);
      if (FAILED(hRes))
      {
        hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_A, &lpPathPropA);
      }
      if (SUCCEEDED(hRes))
      {
        if (lpPathPropW && lpPathPropW->Value.lpszW)
        {
          wzPath = lpPathPropW->Value.lpszW;
        }
        else if (lpPathPropA && lpPathPropA->Value.lpszA)
        {
          szPath = lpPathPropA->Value.lpszA;
        }
      }
      // If this is an Exchange store with an OST path, it's an OST, so get the mapping signature.
      if ((fPrivateExchangeStore || fPublicExchangeStore) && (wzPath || szPath))
      {
        hRes = HrGetOneProp(lpProfSect, PR_MAPPING_SIGNATURE, &lpMappingSig);
      }
    }
  }
  DWORD dwSigHash = NULL;
  if (lpMappingSig && PT_BINARY == PROP_TYPE(lpMappingSig->ulPropTag))
  {
    dwSigHash = ComputeHash(lpMappingSig->Value.bin.cb, lpMappingSig->Value.bin.lpb, NULL, NULL, fPublicExchangeStore);
  }
  DWORD dwEIDHash = ComputeHash(lpEntryID->cb, lpEntryID->lpb, szPath, wzPath, fPublicExchangeStore);
  if (lpdwSigHash) *lpdwSigHash = dwSigHash;
  if (lpdwEIDHash) *lpdwEIDHash = dwEIDHash;
  MAPIFreeBuffer(lpMappingSig);
  MAPIFreeBuffer(lpPathPropA);
  MAPIFreeBuffer(lpPathPropW);
  MAPIFreeBuffer(lpConfigProp);
  if (lpProfSect) lpProfSect->Release();
} // ComputeStoreHash
```

> [!TIP]
> <span data-ttu-id="8fe1f-118">HrEmsmdbUIDFromStore 関数は、ストアを実際に開かずに動作するので、一般的な目的の方法として適しています。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-118">The HrEmsmdbUIDFromStore function works without actually opening the store, so it is a good general purpose approach.</span></span> <span data-ttu-id="8fe1f-119">ただし、store オブジェクトへのポインターが既にある場合は、PR_EMSMDB_SECTION_UID プロパティを読み取って、メッセージストアからプロファイルセクションの GUID を直接取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="8fe1f-119">However, if you have a pointer to the store object already, you can also retrieve the profile section GUID directly from the message store by reading the PR_EMSMDB_SECTION_UID property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fe1f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="8fe1f-120">See also</span></span>

- [<span data-ttu-id="8fe1f-121">通知ベースのストアインデックス作成について</span><span class="sxs-lookup"><span data-stu-id="8fe1f-121">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="8fe1f-122">通知ベースのインデックス作成の MAPI url について</span><span class="sxs-lookup"><span data-stu-id="8fe1f-122">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

