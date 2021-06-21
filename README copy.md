function mint(address minter, string  ArtURI)
    1.mintfee(0.0015 BNB) will sent to fee address
    2.NFT will be minted and sent to minter

    require BNB in minter > mintfee

function mintWithToken(address minter, string  ArtURI)          ** same as mint but use 1 BUSD as fee instead

function burn(uint256 tokenId)
    1.Will delete NFT with tokenId that provided

    require caller to be owner

function setBaseURI(string baseURI)
    function to set the base URI for all token IDs. It is automatically added as a prefix to the value returned in {tokenURI}, or to the token ID if {tokenURI} is empty.

function _setTokenURI(uint256 tokenId, string _tokenURI)
    function to set the base URI for all token IDs

    require tokenId must exist.

function transferMintFeeAddress(address _mintFeeAddr)
    change fee address

    require caller = current fee address

function setMintFeeAmount(uint256 _mintFeeAmount)
    change mint fee amount(BNB) to _mintFeeAmount

    require the new mint fee(BNB) amount can't equal to the older one

function setMintTokenFeeAmount(uint256 _mintTokenFeeAmount)
    change mint fee amount(BUSD) to _mintTokenFeeAmount

    require the new mint fee(BUSD) amount can't equal to the older one

function setMintTokenAddress(address _mintTokenAddr)
    change alternative token to pay mint fee(defult is BUSD)

    require new mint token address can't be the same as the older one
    require new mint token address can't equal to 0

function minterOf(uint256 _tokenId)
    get the minter of NFT at _tokenId

function mintTime(uint256 tokenId)
    get the mint time of NFT at _tokenId

    require tokenId to be exist
