const h2a_fg = "1:33: 30";
const h2a_heretic = "00:00:24 (wr) | 00:00:36 (wr)";
const h2a_armory = "null";
const h2a_cairo = "5:28";
const h2a_outskirts = "4:26";
const h2a_metro = "4:13";
const h2a_arbiter = "2:36";
const h2a_oracle = "12:00";
const h2a_dh = "3:36";
const h2a_regret = "9:31";
const h2a_sacred = "9:01";
const h2a_qz = "7:50";
const h2a_gravemind = "9:06";
const h2a_uprising = "1:54";
const h2a_hc = "1:34";
const h2a_tgj = "9:06";
const h2a_deathless = "Metropolis 13:31";

const times = [
    h2a_fg, h2a_heretic, 
    h2a_armory, h2a_cairo,
    h2a_outskirts, h2a_metro,
    h2a_arbiter, h2a_oracle,
    h2a_dh, h2a_regret,
    h2a_sacred, h2a_qz,
    h2a_gravemind, h2a_uprising,
    h2a_hc, h2a_tgj,
    h2a_deathless ];
const options = [
    "Halo 2/H2", "heretic",
    "armory", "cairo",
    "outskirts/os", "metro",
    "arbiter/arby", "oracle",
    "delta halo/dh", "regret",
    "sacred icon/si", "quarantine zone/qz",
    "gravemind/gm", "uprising",
    "high charity/hc", "the great journey/tgj",
    "deathless" ];
const proper_names = [
    "H2A Full Game", "The Heretic",
    "The Armory", "Cairo Station",
    "Outskirts", "Metropolis",
    "The Arbiter", "The Oracle",
    "Delta Halo", "Regret",
    "Sacred Icon", "Quarantine Zone",
    "Gravemind", "Uprising",
    "High Charity", "The Great Journey",
    "H2A Deathless" ];

var response = "H2A Full Game - " + times[0];

var option = 0;
if(q != "")
{
    for(let i = 0; i < options.length; i++)
    {
        var chunks = options[i].split("/");
        var found = false;
        for(let j = 0; j < chunks.length; j++)
        {
            if(q.toLowerCase() == chunks[j])
            {
                option = i;
                found = true;
                break;
            }
        }
        if(found) break;
    }
    response = proper_names[option] + " - " + times[option];
}

response;