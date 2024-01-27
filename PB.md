const h2a_fg = "null | 1:44:02";
const h2a_heretic = "00:00:24 (wr) | 00:00:36 (wr)";
const h2a_armory = "null | null";
const h2a_cairo = "null | 6:14";
const h2a_outskirts = "null | 4:37";
const h2a_metro = "null | 4:33";
const h2a_arbiter = "null | 2:42";
const h2a_oracle = "null | 12:31";
const h2a_dh = "null | 3:53";
const h2a_regret = "null | 9:53?";
const h2a_sacred = "null | 9:51";
const h2a_qz = "null | 7:54";
const h2a_gravemind = "null | 9:33";
const h2a_uprising = "null | 2:23";
const h2a_hc = "null | 1:51";
const h2a_tgj = "null | 9:06";
const h2a_deathless = "2:31:43 with 46 deaths | Metropolis 13:50 with 0 deaths";

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